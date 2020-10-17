<template>
  <form class="form">
    <div class="form__row">
      <div class="form__control">
        <input
          type="text"
          class="form__input"
          :value="value"
          @input="$emit('input', $event.target.value)"
        />
      </div>

      <div class="form__control form__control--btn">
        <button>Add todo</button>
      </div>
    </div>
  </form>
</template>

<script>
  export default {
    name: 'Form',
    props: {
      value: {
        type: String,
        default: () => '',
      },
    },
  }
</script>

<style lang="scss" scoped>
  .form {
    &__row {
      display: flex;
    }

    &__control {
      flex: 1;

      &--btn {
        flex: unset;
      }
    }

    &__input {
      width: 100%;
    }
  }
</style>
