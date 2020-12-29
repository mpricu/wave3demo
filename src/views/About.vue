<template>
  <div id="app">
    <w-app block>
      <w-table :headers="table.headers" :items="table.items"></w-table>
    </w-app>
  </div>
</template>
<script>
export default {
  setup() {
    const table = {
      headers: [
        { label: "ID", key: "id" },
        { label: "First name", key: "firstName" },
        { label: "Last name", key: "lastName" },
      ],
      items: [
        { id: "1", firstName: "Floretta", lastName: "Sampson" },
        { id: "2", firstName: "Nellie", lastName: "Lynn" },
        { id: "3", firstName: "Rory", lastName: "Bristol" },
        { id: "4", firstName: "Daley", lastName: "Elliott" },
        { id: "5", firstName: "Virgil", lastName: "Carman" },
      ],
    };

    return {
      table,
    };
  },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.w-app {
  font: 14px sans-serif;
  padding: 24px;
}
</style>
