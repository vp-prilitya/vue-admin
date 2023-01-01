<template>
  <div
    class="fixed top-0 z-40 backdrop-blur flex-none transition-colors duration-500 flex justify-between px-10 items-center w-full h-14 border-b border-slate-900/10 shadow-sm"
  >
    <div class="text-xl leading-6 flex items-center">
      <img src="./assets/logo.png" class="mr-2" width="25" alt="" />
      Proctoring
    </div>
    <div class="text-xs font-medium">
      <a href="#" class="bg-blue-200 text-blue-600 px-3 py-1 rounded-full"
        >Logout</a
      >
    </div>
  </div>
  <div class="max-w-8xl mx-auto">
    <div
      class="bg-gray-50 ease-in-out duration-200 top-14 h-screen fixed border-r border-slate-900/10 shadow-inner"
      :class="openSibedar ? 'w-56' : 'w-6'"
    >
      <div
        @click="actionSidebar"
        class="flex absolute -right-3 top-5 w-6 h-6 transition duration-200 bg-white rounded-full border border-slate-900/10 cursor-pointer hover:bg-blue-600 hover:text-white text-gray-500"
      >
        <svg
          class="w-3 h-3 m-auto"
          fill="none"
          stroke="currentColor"
          viewBox="0 0 24 24"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="4 "
            d="M15 19l-7-7 7-7"
          ></path>
        </svg>
      </div>
      <div
        class="space-x-3 px-4 pt-7 transition duration-300"
        :class="openSibedar ? 'flex' : 'hidden'"
      >
        <img
          class="w-12 rounded-full ring-2 ring-gray-200"
          src="https://i.pinimg.com/474x/26/32/ed/2632ed38f455851dd9adf61c89417d90.jpg"
          alt=""
        />
        <div>
          <h2 class="font-semibold">Viraka Prilitya</h2>
          <p class="text-sm text-gray-500">Administrator</p>
        </div>
      </div>
      <div class="px-4 pt-8" :class="openSibedar ? 'block' : 'hidden'">
        <h3 class="text-[11px] pl-4 font-bold text-gray-700 pb-2 uppercase">
          Main Menu
        </h3>
        <ul class="space-y-1">
          <li>
            <a
              href="#"
              class="flex items-center p-2 px-4 text-base font-normal text-gray-700 rounded-lg hover:bg-gray-200"
            >
              <svg
                class="w-5 h-5 text-gray-700"
                fill="none"
                stroke="currentColor"
                viewBox="0 0 24 24"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6"
                ></path>
              </svg>
              <span class="ml-4 text-gray-700 text-[14px]">Dashboard</span>
            </a>
          </li>
          <li>
            <a
              href="#"
              class="flex items-center p-2 px-4 text-base font-normal text-white rounded-lg hover:bg-blue-700 bg-blue-600"
            >
              <svg
                class="w-5 h-5"
                fill="none"
                stroke="currentColor"
                viewBox="0 0 24 24"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M9 20l-5.447-2.724A1 1 0 013 16.382V5.618a1 1 0 011.447-.894L9 7m0 13l6-3m-6 3V7m6 10l4.553 2.276A1 1 0 0021 18.382V7.618a1 1 0 00-.553-.894L15 4m0 13V4m0 0L9 7"
                ></path>
              </svg>
              <span class="ml-4 text-[14px]">Tracking</span>
            </a>
          </li>
          <li>
            <a
              href="#"
              class="flex items-center p-2 px-4 text-base font-normal text-gray-700 rounded-lg hover:bg-gray-200"
            >
              <svg
                class="w-5 h-5"
                fill="none"
                stroke="currentColor"
                viewBox="0 0 24 24"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"
                ></path>
              </svg>
              <span class="ml-4 text-[14px]">Message</span>
            </a>
          </li>
          <li>
            <a
              href="#"
              class="flex items-center p-2 px-4 text-base font-normal text-gray-700 rounded-lg hover:bg-gray-200"
            >
              <svg
                class="w-5 h-5"
                fill="none"
                stroke="currentColor"
                viewBox="0 0 24 24"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M12 6V4m0 2a2 2 0 100 4m0-4a2 2 0 110 4m-6 8a2 2 0 100-4m0 4a2 2 0 110-4m0 4v2m0-6V4m6 6v10m6-2a2 2 0 100-4m0 4a2 2 0 110-4m0 4v2m0-6V4"
                ></path>
              </svg>
              <span class="ml-4 text-[14px]">Setting</span>
            </a>
          </li>
        </ul>
      </div>
    </div>
    <div class="pl-[17em] pt-[5.5em] pr-8 pb-10">
      <span class="text-gray-500 text-sm">Dashboard / Data</span>
      <div class="items-center">
        <h1
          class="inline-block text-2xl font-extrabold text-slate-900 tracking-tight"
        >
          Customizing Spacing
        </h1>
      </div>
      <div class="pt-5 flex justify-between items-center">
        <div class="relative w-56">
          <div
            class="absolute inset-y-0 left-0 flex items-center pl-3 pointer-events-none"
          >
            <svg
              aria-hidden="true"
              class="w-5 h-5 text-gray-500"
              fill="currentColor"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                fill-rule="evenodd"
                d="M8 4a4 4 0 100 8 4 4 0 000-8zM2 8a6 6 0 1110.89 3.476l4.817 4.817a1 1 0 01-1.414 1.414l-4.816-4.816A6 6 0 012 8z"
                clip-rule="evenodd"
              ></path>
            </svg>
          </div>
          <input
            type="text"
            id="simple-search"
            class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full pl-10 p-2.5"
            placeholder="Search"
            required
          />
        </div>
        <div class="">
          <button class="bg-blue-600 text-white px-3 py-1 rounded-md">
            Create
          </button>
        </div>
      </div>
      <div class="pt-8 flex space-x-5">
        <div
          class="max-w-sm p-6 bg-white border border-gray-200 rounded-lg shadow-md"
        >
          <svg
            class="w-10 h-10 mb-2 text-gray-500"
            aria-hidden="true"
            fill="currentColor"
            viewBox="0 0 20 20"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              fill-rule="evenodd"
              d="M5 5a3 3 0 015-2.236A3 3 0 0114.83 6H16a2 2 0 110 4h-5V9a1 1 0 10-2 0v1H4a2 2 0 110-4h1.17C5.06 5.687 5 5.35 5 5zm4 1V5a1 1 0 10-1 1h1zm3 0a1 1 0 10-1-1v1h1z"
              clip-rule="evenodd"
            ></path>
            <path
              d="M9 11H3v5a2 2 0 002 2h4v-7zM11 18h4a2 2 0 002-2v-5h-6v7z"
            ></path>
          </svg>
          <a href="#">
            <h5
              class="mb-2 text-2xl font-semibold tracking-tight text-gray-900"
            >
              Need a help in Claim?
            </h5>
          </a>
          <p class="mb-3 font-normal text-gray-500 dark:text-gray-400">
            Go to this step by step guideline process on how to certify for your
            weekly benefits:
          </p>
        </div>

        <div
          class="max-w-sm p-6 bg-white border border-gray-200 rounded-lg shadow-md dark:bg-gray-800 dark:border-gray-700"
        >
          <svg
            class="w-10 h-10 mb-2 text-gray-500 dark:text-gray-400"
            aria-hidden="true"
            fill="currentColor"
            viewBox="0 0 20 20"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              fill-rule="evenodd"
              d="M5 5a3 3 0 015-2.236A3 3 0 0114.83 6H16a2 2 0 110 4h-5V9a1 1 0 10-2 0v1H4a2 2 0 110-4h1.17C5.06 5.687 5 5.35 5 5zm4 1V5a1 1 0 10-1 1h1zm3 0a1 1 0 10-1-1v1h1z"
              clip-rule="evenodd"
            ></path>
            <path
              d="M9 11H3v5a2 2 0 002 2h4v-7zM11 18h4a2 2 0 002-2v-5h-6v7z"
            ></path>
          </svg>
          <a href="#">
            <h5
              class="mb-2 text-2xl font-semibold tracking-tight text-gray-900 dark:text-white"
            >
              Need a help in Claim?
            </h5>
          </a>
          <p class="mb-3 font-normal text-gray-500 dark:text-gray-400">
            Go to this step by step guideline process on how to certify for your
            weekly benefits:
          </p>
          <a
            href="#"
            class="inline-flex items-center text-blue-600 hover:underline"
          >
            See our guideline
            <svg
              class="w-5 h-5 ml-2"
              fill="currentColor"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M11 3a1 1 0 100 2h2.586l-6.293 6.293a1 1 0 101.414 1.414L15 6.414V9a1 1 0 102 0V4a1 1 0 00-1-1h-5z"
              ></path>
              <path
                d="M5 5a2 2 0 00-2 2v8a2 2 0 002 2h8a2 2 0 002-2v-3a1 1 0 10-2 0v3H5V7h3a1 1 0 000-2H5z"
              ></path>
            </svg>
          </a>
        </div>
      </div>
      <div class="overflow-x-auto relative shadow-md sm:rounded-lg mt-7">
        <table class="w-full text-sm text-left text-gray-500">
          <thead class="text-xs text-gray-700 uppercase bg-gray-50">
            <tr>
              <th scope="col" class="py-3 px-6">Product name</th>
              <th scope="col" class="py-3 px-6">Color</th>
              <th scope="col" class="py-3 px-6">Category</th>
              <th scope="col" class="py-3 px-6">Price</th>
              <th scope="col" class="py-3 px-6">
                <span class="sr-only">Edit</span>
              </th>
            </tr>
          </thead>
          <tbody>
            <tr class="bg-white border-b hover:bg-gray-50">
              <th
                scope="row"
                class="py-4 px-6 font-medium text-gray-900 whitespace-nowrap"
              >
                Apple MacBook Pro 17"
              </th>
              <td class="py-4 px-6">Sliver</td>
              <td class="py-4 px-6">Laptop</td>
              <td class="py-4 px-6">$2999</td>
              <td class="py-4 px-6 text-right">
                <a href="#" class="font-medium text-blue-600 hover:underline"
                  >Edit</a
                >
              </td>
            </tr>
            <tr class="bg-white border-b hover:bg-gray-50">
              <th
                scope="row"
                class="py-4 px-6 font-medium text-gray-900 whitespace-nowrap"
              >
                Microsoft Surface Pro
              </th>
              <td class="py-4 px-6">White</td>
              <td class="py-4 px-6">Laptop PC</td>
              <td class="py-4 px-6">$1999</td>
              <td class="py-4 px-6 text-right">
                <a href="#" class="font-medium text-blue-600 hover:underline"
                  >Edit</a
                >
              </td>
            </tr>
            <tr class="bg-white hover:bg-gray-50">
              <th
                scope="row"
                class="py-4 px-6 font-medium text-gray-900 whitespace-nowrap"
              >
                Magic Mouse 2
              </th>
              <td class="py-4 px-6">Black</td>
              <td class="py-4 px-6">Accessories</td>
              <td class="py-4 px-6">$99</td>
              <td class="py-4 px-6 text-right">
                <a href="#" class="font-medium text-blue-600 hover:underline"
                  >Edit</a
                >
              </td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </div>
</template>

<script>
import { ref } from "@vue/reactivity";

export default {
  setup() {
    const openSibedar = ref(true);

    const actionSidebar = () => {
      openSibedar.value = !openSibedar.value;
    };

    return {
      openSibedar,
      actionSidebar,
    };
  },
};
</script>
