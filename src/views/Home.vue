<script setup>
import Navbar from '@/components/Navbar.vue';
</script>

<template>
  <div class="bg-[#547DA9] h-screen w-full">
    <Navbar />
    <div class="w-full flex">
      <div class="w-[300px] h-full md:flex hidden"></div>
      <div class="w-full h-[600px] bg-[#EEF4FA] border">
        <div
          class="w-full bg-[#D3E4F4] flex flex-wrap-reverse items-center md:justify-between justify-center p-2"
        >
          <div class="my-2 md:my-0">
            <button class="btn bg-[#547DA9] capitalize mr-4 border-none">
              Create a groupe
            </button>
            <button class="btn text-[#547DA9] bg-white capitalize border-none">
              Create a goods
            </button>
          </div>
          <div class="relative">
            <input
              type="text"
              class="input w-[350px] placeholder:text-[#547DA9]"
              placeholder="Search"
            />
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="h-6 w-6 absolute top-3 right-1 text-[#547DA9]"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"
              />
            </svg>
          </div>
        </div>
        <div class="w-full pl-6">
          <div class="overflow-x-auto">
            <table class="table w-full">
              <thead class="">
                <tr>
                  <th
                    class="w-4/5 bg-[#EEF4FA] font-light text-[#547DA9] capitalize"
                  >
                    Name
                  </th>
                  <th class="bg-[#EEF4FA] font-light text-[#547DA9] capitalize">
                    Balance
                  </th>
                  <th class="bg-[#EEF4FA] font-light text-[#547DA9] capitalize">
                    Price
                  </th>
                </tr>
              </thead>
              <tbody>
                <tr v-for="item in items" :key="item">
                  <td class="flex items-center text-[#547DA9]" @click="alert">
                    <svg
                      v-if="item.childrens"
                      xmlns="http://www.w3.org/2000/svg"
                      class="h-6 w-6 mr-2"
                      fill="none"
                      viewBox="0 0 24 24"
                      stroke="currentColor"
                    >
                      <path
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        stroke-width="2"
                        d="M5 19a2 2 0 01-2-2V7a2 2 0 012-2h4l2 2h4a2 2 0 012 2v1M5 19h14a2 2 0 002-2v-5a2 2 0 00-2-2H9a2 2 0 00-2 2v5a2 2 0 01-2 2z"
                      />
                    </svg>
                    {{ item.name }}
                    <div></div>
                  </td>
                  <td>{{ item.balance }}$</td>
                  <td>{{ item.price }}$</td>
                </tr>
                <div v-if="showChildren">
                  <tr v-for="child in item.childrens" :key="child">
                    <td>{{ child.balance }}$</td>
                    <td>{{ child.price }}$</td>
                  </tr>
                </div>
              </tbody>
            </table>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      items: [
        {
          id: 1,
          name: 'Groupe 1',
          balance: 0,
          price: 340,
          childrens: [
            {
              id: 1,
              name: 'Goods 1',
              balance: 0,
              price: 340,
            },
            { id: 2, name: 'Goods 2', balance: 0, price: 340 },
          ],
        },
        {
          id: 1,
          name: 'Groupe 2',
          balance: 0,
          price: 340,
          childrens: [
            {
              id: 1,
              name: 'Goods 1',
              balance: 0,
              price: 340,
            },
            { id: 2, name: 'Goods 2', balance: 0, price: 340 },
          ],
        },
        {
          id: 1,
          name: 'Groupe 3',
          balance: 0,
          price: 340,
          childrens: [
            {
              id: 1,
              name: 'Goods 1',
              balance: 0,
              price: 340,
            },
            { id: 2, name: 'Goods 2', balance: 0, price: 340 },
          ],
        },
        {
          id: 1,
          name: 'Groupe 4',
          balance: 0,
          price: 340,
          childrens: [
            {
              id: 1,
              name: 'Goods 1',
              balance: 0,
              price: 340,
            },
            { id: 2, name: 'Goods 2', balance: 0, price: 340 },
          ],
        },
        {
          id: 1,
          name: 'Groupe 5',
          balance: 0,
          price: 340,
          childrens: [
            {
              id: 1,
              name: 'Goods 1',
              balance: 0,
              price: 340,
            },
            { id: 2, name: 'Goods 2', balance: 0, price: 340 },
          ],
        },
        {
          id: 1,
          name: 'Groupe 6',
          balance: 0,
          price: 340,
          childrens: [
            {
              id: 1,
              name: 'Goods 1',
              balance: 0,
              price: 340,
            },
            { id: 2, name: 'Goods 2', balance: 0, price: 340 },
          ],
        },
        {
          id: 1,
          name: 'Groupe 7',
          balance: 0,
          price: 340,
          childrens: [
            {
              id: 1,
              name: 'Goods 1',
              balance: 0,
              price: 340,
            },
            { id: 2, name: 'Goods 2', balance: 0, price: 340 },
          ],
        },
      ],
    };
  }
};
</script>
