<template>
  <table>
    <tr>
      <th
        v-for="tableHead in tableHeads"
        class="text-3xl font-bold underline bg-blue-50"
      >
        {{ tableHead }}
      </th>
    </tr>
    <tr v-for="(diff, index) in difference">
      <td>{{ index + 1 }}</td>
      <td>{{ diff }}</td>
      <td>{{ points[index] }}</td>
      <!-- <td>{{ point[index] }}</td> -->
    </tr>
  </table>
  <div class="input-container flex flex-col">
    <input type="text" placeholder="Tordifferenz" v-model="difference" />
    <input type="text" placeholder="Punkte" v-model="points" />
  </div>
</template>
<script>
export default {
  name: "Home",
  data() {
    return {
      differenceInput: "",
      pointsInput: "",
      tableHeads: ["ID", "Tordifferenz", "Punkte"],
      difference: [],
      points: [],
    };
  },
  methods: {},
};
</script>
