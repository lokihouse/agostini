<template>
  <q-page>
    <div class="tw-flex tw-justify-center tw-pt-10">
      <div class="tw-w-[300px]">
        <q-card>
          <q-card-section>
            <div class="">
              <q-form @submit="onSubmit" @reset="onReset" class="q-gutter-md">
                <q-input filled v-model="username" label="Usuário ou Email *" />

                <q-input filled type="password" v-model="password" label="Senha *"/>

                <div class="tw-space-y-2">
                  <q-btn class="full-width" label="Acessar" type="submit" color="primary"/>
                </div>
              </q-form>
            </div>
          </q-card-section>
        </q-card>
      </div>
    </div>
  </q-page>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';

export default defineComponent({
  name: 'IndexPage',

  setup() {
    return {
      username: ref(''),
      password: ref(''),
      onSubmit: () => {
        console.log('onSub')
      },
      onReset: () => {
        console.log('onRes')
      }
    }
  }
});
</script>
