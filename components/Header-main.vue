<!-- https://www.npmjs.com/package/vue-typed-js -->
<template>
  <div>
    <div>
      <h1 class="header-main">
        {{ $t('header.welcome') }}
        <br />
        {{ $t('header.tellmemore1') }}
        <vue-typed-js
          :typeSpeed="50"
          :backSpeed="50"
          :backDelay="1000"
          :strings="[
            $t('header.company'),
            $t('header.role'),
            $t('header.stack'),
            $t('header.resp'),
            $t('header.renum'),
            $t('header.benefits'),
          ]"
          :loop="true"
          :smartBackspace="false"
          :cursorChar="'_'"
        >
          <div>
            {{ $t('header.tellmemore2') }}
            <span class="typing header-main-typing"></span>
          </div>
        </vue-typed-js>
      </h1>
    </div>
    <div class="mt-5">
      <p class="header-sub-text">
        {{ $t('header.sub1') }} {{ $t('header.carmake')
        }}{{ $t('header.disappointment') }}
      </p>
    </div>
  </div>
</template>

<script>
import { VueTypedJs } from 'vue-typed-js'

export default {
  components: {
    VueTypedJs,
  },
  data() {
    return {}
  },
}
</script>

<style scoped>
@media screen {
  .header-main {
    font-size: 3rem;
    font-weight: 600;
  }

  .header-sub-text {
    font-size: 2rem;
    font-weight: 300;
  }
}

@media screen and (max-width: 996px) {
  .header-main {
    font-size: 2rem;
    font-weight: 600;
  }

  .header-sub-text {
    font-size: 1.5rem;
    font-weight: 300;
  }
}

.header-main-typing {
  color: #f5428a;
}
</style>
