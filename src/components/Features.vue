<template>
  <section class="container px-5 py-12 mx-auto text-gray-600 body-font">
    <div class="">
      <TypeHeading class="mb-4 text-gray-400" tag="div">
        My Pollen Components
      </TypeHeading>
      <div class="mb-4">
        <BaseButton @click="handleButtonClick" size="giant" variant="primary">
          My Button
        </BaseButton>
      </div>
      <div class="mb-4">
        <TextInput
          @input="handleTextInputChange"
          placeholder="Pollen TextInput"
        />
      </div>
      <div class="mb-4">
        <BaseIcon icon="cogsSolid" />
        <BaseIcon icon="cogsSolid" class="text-white mx-4" />
        <BaseIcon icon="cogsSolid" class="text-black" />
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import { BaseButton, TypeHeading, TextInput, BaseIcon } from "@bambee/pollen";

export default {
  components: {
    BaseButton,
    TypeHeading,
    TextInput,
    BaseIcon,
  },
  setup() {
    const handleTextInputChange = (event: InputEvent) => {
      console.log("Text Input Event", event);
    };

    const handleButtonClick = () => {
      console.log("Base Button Clicked");
    };

    return {
      handleTextInputChange,
      handleButtonClick,
    };
  },
};
</script>
