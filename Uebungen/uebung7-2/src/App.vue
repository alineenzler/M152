<template>
  <div class="content"> 
    <h1>Uebung 7-2: Grades</h1>

    <!-- <h3>Durchschnitt: {{ schoolAverage }} Mangelpunkte: {{ schoolMinus }}</h3> -->

    <ul>
      <li v-for:="grade in grades">{{ grade.name }} {{ grade.grades }} <r>Durchschnitt {{ gradeAverage }}</r></li>
    </ul>

    <!-- <input v-model="newGrade"  type="number" placeholder="Note" />
    <input v-model="newSubject" placeholder="Fach"/>
    <button class="add-button" v-on:click="addExam()">Eintrag hinzufügen</button> -->
  </div>
</template>

<script>
  export default {
    name: 'App',
    data: function() {
      return {
        grades: [
          {
            name: "Mathematik",
            grades: [5,4.7,3.5,4.1] 
          },
          {
            name: "Geschichte",
            grades: [5.5,4.9,5.75] 
          },
          {
            name: "Physik",
            grades: [2,2.7,4.3] 
          },
          {
            name: "Deutsch",
            grades: [4.25,4.1,3.5] 
          },
        ]
        // newGrade: ''
      }
    },
    computed: {
      gradeAverage: function() {
        
      }
    }
    // },
    // methods: {
    //   addExam: function() {
    //     this.grades.push({
    //       name: this.newSubject = '',
    //       grades: parseInt(this.newGrade)
    //     });
    //     this.newSubject = '';
    //     this.newGrade = 0;
    //   }
    // }
}
</script> 

<style lang="scss">
.content {
  margin: 20px;
}

input {
  margin: 5px;
}

li {
  width: 440px;
}

r {
    float: right;
    text-align: right;
}

.add-button {
  margin: 5px;
}
</style>
