<template>
  <div>
    newEntries: {{ newEntries }}
    <table>
      <tr v-for="(fund, index) in defaultFunds" :key="index">
      
        <td>{{ fund.name }}</td>
        <td>
          <input v-model="newEntries[index].id" name="entryFund" type="text" />
        </td>
        <td>
          <input
            v-model="newEntries[index].amount"
            name="entryFund"
            type="text"
          />
        </td>
      </tr>
    </table>
  </div>
</template>

<script setup>
export default {
  data() {
    return {
      newEntries: [{}, {}],

    defaultFunds: [
      {
        id: 100,
        name: "fund 0",
      },
      {
        id: 101,
        name: "fund 1",
      },
    ]
    }
    
  },
  methods: {},
};
</script>
