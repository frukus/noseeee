<template>
  <div>
    <h1>hh</h1>
    <cv-list v-for="m of materias" :key="m.id">
      <cv-list-item>{{ m.name }}</cv-list-item>
    </cv-list>
    <cv-data-table :columns="columns2" :rows="colum" title="Materias" helper-text="Data has been requested fetched">
      <cv-data-table-row v-for="w in materias" :key="w.id">
        <cv-data-table-cell>
          {{ w.name }}
        </cv-data-table-cell>
      </cv-data-table-row>
    </cv-data-table>
  </div>
</template>

<script>
export default {
  data () {
    return {
      ordered: false,
      colum: 5,
      columns2: [
        'Nombre Materia',
        'Hora inicio',
        'Hora fin'
      ],
      materias: [{ name: 'mate', semestre: '2', inicio: '14:00', fin: '15:00' }, { name: 'ma', semestre: '2', inicio: '14:00', fin: '15:00' }]
    }
  }
}
</script>

<style>
</style>
