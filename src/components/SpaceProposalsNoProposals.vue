<script setup lang="ts">
import { ExtendedSpace } from '@/helpers/interfaces';

defineProps<{
  space: ExtendedSpace;
}>();
</script>
<template>
  <div class="mb-3 text-center">
    <BaseBlock class="pt-1">
      <div class="mb-3">
        {{ $t('noResultsFound') }}
      </div>
      <router-link :to="{ name: 'spaceCreate', params: { step: 0 } }">
        <BaseButton>
          {{ $t('proposals.createProposal') }}
        </BaseButton>
      </router-link>
    </BaseBlock>
  </div>
</template>
