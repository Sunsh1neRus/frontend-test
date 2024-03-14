<template>
  <div class="form-builder">
    <!-- Должно собираться автоматически, а не руками как сейчас, согласно конфигу   -->
    <form @submit.prevent="onSubmit">
      <form-input label="Имя"  />
      <form-select label="Гендер" :options="[{ value: 'male', text: 'Мужской' }, { value: 'female', text: 'Женский', selected: true }]" />
      <form-radio label="Возраст" :options="[{ value: '10', text: 'Мужской' }, { value: '20', text: 'Женский', selected: true }]" />
      <form-password label="Пароль" />

      <button type="submit">Отправить</button>
      <button type="reset">Стереть</button>
    </form>
  </div>
</template>

<script>
import FormInput from "@/components/form-items/FormInput.vue";
import FormSelect from "@/components/form-items/FormSelect.vue";
import FormRadio from "@/components/form-items/FormRadio.vue";
import FormPassword from "@/components/form-items/FormPassword.vue";

export default {
  name: "FormBuilder",

  methods: {
    onSubmit() {
      alert('Submit')
    }
  },
  components: {FormPassword, FormRadio, FormSelect, FormInput}
}
</script>

<style scoped>

</style>
