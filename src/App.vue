<template>
  <div class="fixed inset-0 overflow-hidden bg-indigo-100">
    <transition
      enter-active-class="transform transition ease-in-out duration-500 sm:duration-700"
      enter-from-class="translate-x-full"
      enter-to-class="translate-x-0"
      leave-active-class="transform transition ease-in-out duration-500 sm:duration-700"
      leave-from-class="translate-x-0"
      leave-to-class="translate-x-full"
    >
      <div
        v-if="open"
        class="absolute inset-0 overflow-y-auto overflow-x-hidden"
      >
        <section @keydown.esc="setOpen" class="absolute inset-y-0 right-0 flex">
          <div aria-hidden class="w-10"></div>
          <div class="flex-1 w-full max-w-xs sm:max-w-md">
            <div class="min-h-full flex flex-col bg-white shadow-xl">
              <header class="space-y-1 py-6 px-4 bg-indigo-700">
                <div class="flex items-center justify-between">
                  <h2 class="text-lg leading-7 font-medium text-white">
                    New Project
                  </h2>
                  <button
                    @click="setOpen"
                    aria-label="Close panel"
                    class="text-indigo-200 hover:text-white transition ease-in-out duration-150"
                  >
                    <svg
                      class="h-6 w-6"
                      xmlns="http://www.w3.org/2000/svg"
                      viewBox="0 0 20 20"
                      fill="currentColor"
                    >
                      <path
                        fill-rule="evenodd"
                        d="M4.293 4.293a1 1 0 011.414 0L10 8.586l4.293-4.293a1 1 0 111.414 1.414L11.414 10l4.293 4.293a1 1 0 01-1.414 1.414L10 11.414l-4.293 4.293a1 1 0 01-1.414-1.414L8.586 10 4.293 5.707a1 1 0 010-1.414z"
                        clip-rule="evenodd"
                      />
                    </svg>
                  </button>
                </div>
                <div>
                  <p class="text-sm leading-5 text-indigo-300">
                    Get started by filling in the information below to create
                    your new project.
                  </p>
                </div>
              </header>
              <div
                class="flex-1 flex flex-col justify-between divide-y divide-gray-200"
              >
                <div class="px-4 divide-y divide-gray-200">
                  <div class="space-y-6 pt-6 pb-5">
                    <div class="space-y-1">
                      <label
                        for="project_name"
                        class="block text-sm font-medium text-gray-900"
                        >Project name</label
                      >
                      <input
                        autofocus
                        type="text"
                        name="project_name"
                        id="project_name"
                        class="focus:ring-indigo-500 focus:border-indigo-500 block w-full shadow-sm sm:text-sm border-gray-300 rounded-md transition ease-in-out duration-150"
                      />
                    </div>
                    <div class="space-y-1">
                      <label
                        for="description"
                        class="block text-sm font-medium text-gray-900"
                      >
                        Description
                      </label>
                      <div>
                        <textarea
                          id="description"
                          name="description"
                          rows="4"
                          class="shadow-sm focus:ring-indigo-500 focus:border-indigo-500 mt-1 block w-full sm:text-sm border-gray-300 rounded-md transition ease-in-out duration-150"
                        ></textarea>
                      </div>
                    </div>
                    <div class="space-y-2">
                      <h3 class="text-sm font-medium text-gray-900">
                        Team Members
                      </h3>
                      <div>
                        <div class="flex space-x-2">
                          <a href="#"
                            ><img
                              class="inline-block h-8 w-8 rounded-full"
                              src="https://images.unsplash.com/photo-1491528323818-fdd1faba62cc?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
                              alt=""
                          /></a>
                          <a href="#"
                            ><img
                              class="inline-block h-8 w-8 rounded-full"
                              src="https://images.unsplash.com/photo-1550525811-e5869dd03032?ixlib=rb-1.2.1&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
                              alt=""
                          /></a>
                          <a href="#"
                            ><img
                              class="inline-block h-8 w-8 rounded-full"
                              src="https://images.unsplash.com/photo-1500648767791-00dcc994a43e?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2.25&w=256&h=256&q=80"
                              alt=""
                          /></a>
                          <a href="#"
                            ><img
                              class="inline-block h-8 w-8 rounded-full"
                              src="https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
                              alt=""
                          /></a>
                          <a href="#"
                            ><img
                              class="inline-block h-8 w-8 rounded-full"
                              src="https://images.unsplash.com/photo-1497551060073-4c5ab6435f12?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
                              alt=""
                          /></a>
                          <button
                            type="button"
                            class="inline-flex h-8 w-8 items-center justify-center rounded-full border-2 border-dashed border-gray-200 text-gray-400 hover:text-gray-500 transition ease-in-out duration-150"
                            aria-label="Add team member"
                          >
                            <svg
                              class="h-6 w-6"
                              xmlns="http://www.w3.org/2000/svg"
                              fill="none"
                              viewBox="0 0 24 24"
                              stroke="currentColor"
                            >
                              <path
                                stroke-linecap="round"
                                stroke-linejoin="round"
                                stroke-width="2"
                                d="M12 6v6m0 0v6m0-6h6m-6 0H6"
                              />
                            </svg>
                          </button>
                        </div>
                      </div>
                    </div>
                    <fieldset class="space-y-2">
                      <legend class="text-sm font-medium text-gray-900">
                        Privacy
                      </legend>
                      <div class="space-y-4">
                        <div class="relative flex items-start">
                          <div class="flex items-center h-5">
                            <input
                              id="privacy_public"
                              name="privacy"
                              type="radio"
                              class="focus:ring-indigo-500 h-4 w-4 text-indigo-600 border-gray-300"
                            />
                          </div>
                          <div class="ml-3 text-sm">
                            <label
                              for="privacy_public"
                              class="font-medium text-gray-900"
                              >Public access</label
                            >
                            <p class="text-gray-500">
                              Everyone with the link will see this project.
                            </p>
                          </div>
                        </div>
                        <div class="relative flex items-start">
                          <div class="flex items-center h-5">
                            <input
                              id="privacy_private-to-project"
                              name="privacy"
                              type="radio"
                              class="focus:ring-indigo-500 h-4 w-4 text-indigo-600 border-gray-300"
                            />
                          </div>
                          <div class="ml-3 text-sm">
                            <label
                              for="privacy_private-to-project"
                              aria-describedby="private_private-to-project_description"
                              class="font-medium text-gray-900"
                              >Private to project members</label
                            >
                            <p
                              id="privacy_private-to-project_description"
                              class="text-gray-500"
                            >
                              Only members of this project would be able to
                              access.
                            </p>
                          </div>
                        </div>
                        <div class="relative flex items-start">
                          <div class="flex items-center h-5">
                            <input
                              id="privacy_private"
                              name="privacy"
                              type="radio"
                              class="focus:ring-indigo-500 h-4 w-4 text-indigo-600 border-gray-300"
                            />
                          </div>
                          <div class="ml-3 text-sm">
                            <label
                              for="privacy_private"
                              aria-describedby="privacy_private_description"
                              class="font-medium text-gray-900"
                              >Private to you</label
                            >
                            <p
                              id="privacy_private_description"
                              class="text-gray-500"
                            >
                              You are the only one able to access this project.
                            </p>
                          </div>
                        </div>
                      </div>
                    </fieldset>
                  </div>
                  <div class="space-y-4 pt-4 pb-6">
                    <div class="flex text-sm leading-5">
                      <a
                        href="#"
                        class="group space-x-2 inline-flex items-center font-medium text-indigo-600 hover:text-indigo-500 transition ease-in-out duration-150"
                      >
                        <svg
                          class="h-5 w-5 text-indigo-500 group-hover:text-indigo-400 transition ease-in-out duration-150"
                          xmlns="http://www.w3.org/2000/svg"
                          fill="none"
                          viewBox="0 0 24 24"
                          stroke="currentColor"
                        >
                          <path
                            stroke-linecap="round"
                            stroke-linejoin="round"
                            stroke-width="2"
                            d="M13.828 10.172a4 4 0 00-5.656 0l-4 4a4 4 0 105.656 5.656l1.102-1.101m-.758-4.899a4 4 0 005.656 0l4-4a4 4 0 00-5.656-5.656l-1.1 1.1"
                          />
                        </svg>
                        <span>Copy link</span>
                      </a>
                    </div>
                    <div class="flex text-sm leading-5">
                      <a
                        href="#"
                        class="group space-x-2 inline-flex items-center text-gray-500 hover:text-gray-900 transition ease-in-out duration-150"
                      >
                        <svg
                          class="h-5 w-5 text-gray-400 group-hover:text-gray-500 transition ease-in-out duration-150"
                          xmlns="http://www.w3.org/2000/svg"
                          viewBox="0 0 20 20"
                          fill="currentColor"
                        >
                          <path
                            fill-rule="evenodd"
                            d="M18 10a8 8 0 11-16 0 8 8 0 0116 0zm-8-3a1 1 0 00-.867.5 1 1 0 11-1.731-1A3 3 0 0113 8a3.001 3.001 0 01-2 2.83V11a1 1 0 11-2 0v-1a1 1 0 011-1 1 1 0 100-2zm0 8a1 1 0 100-2 1 1 0 000 2z"
                            clip-rule="evenodd"
                          />
                        </svg>
                        <span>Learn more about sharing</span>
                      </a>
                    </div>
                  </div>
                </div>
                <div class="px-4 py-4 space-x-4 flex justify-end">
                  <button
                    @click="setOpen"
                    type="button"
                    class="w-full inline-flex justify-center rounded-md border border-gray-300 shadow-sm px-4 py-2 bg-white text-base font-medium text-gray-700 hover:bg-gray-50 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500 sm:mt-0 sm:ml-3 sm:w-auto sm:text-sm"
                  >
                    Cancel
                  </button>
                  <button
                    type="button"
                    class="w-full inline-flex justify-center rounded-md border border-transparent shadow-sm px-4 py-2 bg-indigo-600 text-base font-medium text-white hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500 sm:ml-3 sm:w-auto sm:text-sm"
                  >
                    Create
                  </button>
                </div>
              </div>
            </div>
          </div>
        </section>
      </div>
    </transition>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      open: true,
    };
  },
  methods: {
    setOpen() {
      this.open = false;
      setTimeout(() => {
        this.open = true;
      }, 1000);
    },
  },
};
</script>
