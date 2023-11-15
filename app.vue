<script lang="ts" setup>
function importsCorrectType(example: WorkingExample) {
  // parameter imported in .nuxt/types/imports.d.ts correctly:
  // export type { WorkingExample } from '../../types/workingExample'
}

function doesNotImportCorrectType(example: NotWorkingExample) {
  // parameter imported in .nuxt/types/imports.d.ts incorrectly with an absolute path, cannot be inferred:
  // export type { NotWorkingExample } from 'C:/Users/m.mustermann/source/repos/PoCs/nuxt-bugs/type-only-import-issue/types/notWorkingExample.ts'
}
</script>

<template>
  <div>
    <NuxtWelcome />
  </div>
</template>
