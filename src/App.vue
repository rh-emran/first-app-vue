<template>
  <div class="container mx-auto">
    <h2 class="font-bold text-red-500 underline mb-4">{{ msg }}</h2>
    <div
      v-for="user in users"
      :key="user.id"
      class="shadow p-4 mb-4 border border-gray-200"
    >
      <h1>User Id: {{ user.id }}</h1>
      <h2>Name: {{ user.name }}</h2>
      <p>Age: {{ user.age }}</p>
      <p>Gender: {{ user.gender }}</p>
    </div>
    <button @click="test" class="px-4 py-2 bg-gray-200 rounded-md">
      Change Title
    </button>
    <button
      @click="count++"
      class="ml-4 border border-blue-500 px-4 py-2 rounded-md"
    >
      You click {{ count }} times
    </button>
  </div>
</template>
[vue/valid-v-on] 'v-on' directives require a value or verb modifi

<script>
export default {
  name: "App",
  data() {
    return {
      msg: "User List:",
      count: 0,
      users: [
        {
          id: 1,
          name: "John",
          age: 20,
          gender: "male",
        },
        {
          id: 2,
          name: "Jane",
          age: 24,
          gender: "female",
        },
        {
          id: 3,
          name: "Jimmy",
          age: 16,
          gender: "male",
        },
      ],
    };
  },
  methods: {
    test() {
      this.msg = "New title for user list:";
    },
  },
};
</script>
