<template>
  <main class="orchestrate">
    <section class="hero">
      <div class="grid">
        <div class="media">
          <NuxtImg src="/landing/company/teams/team.png" alt="Team Image" class="image" width="686" height="456" />
        </div>
        <div class="content">
          <h1 class="title">
            Orchestration for<br>
            Every Developer,<br>
            <span class="gradient">Everywhere.</span>
          </h1>
          <p class="text">
            We're redefining orchestration for developers everywhere —
            challenging the status quo and traditional limitations. Kestra
            empowers engineers to orchestrate any workflow, in any
            language, on any infrastructure, delivering unparalleled freedom
            and flexibility. By simplifying complexity and eliminating
            constraints, we enable developers to build faster, and collaborate
            freely without compromise.
          </p>
        </div>
        <NuxtImg src="/landing/company/teams/line.svg" alt="Connecting Line" class="line" width="224" height="268" />
        <NuxtImg src="/landing/company/teams/flare.svg" alt="Flare Effect" class="flare" />
        <NuxtImg src="/landing/company/teams/flare.svg" alt="Flare Effect 2" class="flare-2" />
      </div>
    </section>

    <section class="trust">
      <div class="divider">
        <NuxtImg src="/landing/company/teams/Logo_EE.png" alt="Kestra Logo" class="logo" width="119" height="109" />
        <NuxtImg src="/landing/company/teams/black-ellipse.svg" alt="Section Divider" width="228" height="135" />
      </div>

      <div class="container" data-aos="fade-up">
        <div class="content">
          <h2 class="title" data-aos="fade-up" data-aos-delay="200">
            Trusted by <span class="gradient">Enterprises</span> Worldwide
          </h2>

          <p class="text-white" data-aos="fade-up" data-aos-delay="300">
            <strong>We are excited</strong> to see how <strong>Kestra</strong> transform the way<br>
            organizations approach orchestration.
          </p>
          <p class="text-white" data-aos="fade-up" data-aos-delay="400">
            We believe that <strong>Kestra's potential is limitless</strong>, and we<br>
            are eager to explore new <strong>opportunities</strong> and<br>
            <strong>partnerships</strong> as we move forward.
          </p>

          <div class="logos" data-aos="fade-up" data-aos-delay="400">
            <div class="grid">
              <NuxtImg
                v-for="(logo, index) in companyLogos"
                :key="logo.name"
                :src="logo.src"
                :alt="logo.name"
                :width="logo.width"
                :height="logo.height"
                :data-aos-delay="500 + (index * 100)"
              />
            </div>
          </div>
        </div>
      </div>
    </section>
  </main>
</template>

<script setup lang="ts">
const companyLogos = [
  { name: "Apple", src: "/landing/company/teams/apple.svg", width: 38, height: 45 },
  { name: "Fila", src: "/landing/companies/fila.svg", width: 60, height: 22 },
  { name: "Axiom", src: "/landing/company/teams/acxiom.svg", width: 102, height: 23 },
  { name: "Battelle", src: "/landing/company/teams/Battelle.svg", width: 101, height: 17 },
  { name: "L'Oreal", src: "/landing/company/teams/loreal.svg", width: 115, height: 20 },
]
</script>

<style lang="scss" scoped>
@import "../../assets/styles/variable";

.orchestrate {
  width: 100%;
  position: relative;

  .hero {
    padding: 2rem 0 170px;
    display: flex;
    align-items: start;
    justify-content: center;
    position: relative;
    background-attachment: fixed;

    @include media-breakpoint-up(md) {
      padding: 33px 64px 170px;
    }

    @include media-breakpoint-up(xxl) {
      padding: 133px 12rem 170px;
    }

    .grid {
      width: min(1140px, 100%);
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 102px;
      position: relative;

      @media (max-width: 1399px) {
        grid-template-columns: 1fr;
        gap: 2rem;
        padding: 0 40px;
      }

      .media {
        position: relative;
        width: 100%;
        max-width: 554px;
        aspect-ratio: 554/414;
        border: 1px solid;
        border-image-source: linear-gradient(91.19deg, #474450 1.02%, rgba(55, 53, 63, 0.37) 66.77%);
        border-image-slice: 1;
        z-index: 2;
        display: flex;
        align-items: center;
        justify-content: center;

        @media (max-width: 1399px) {
          order: 2;
        }

        @media (min-width: 768px) and (max-width: 1399px) {
          margin: 0 auto;
        }

        @media (max-width: 767px) {
          max-width: none;
          width: calc(100% + 40px);
          margin: 0 -20px;
        }

        .image {
          width: 100%;
          height: 100%;
          object-fit: cover;
        }
      }

      .content {
        padding: 2rem 0;

        @media (max-width: 1399px) {
          display: flex;
          flex-direction: column;
          align-items: center;
          text-align: center;
          order: 1;
          padding: 0;
        }

        .title {
          font-family: 'Public Sans';
          font-weight: 600;
          font-size: 48px;
          line-height: 1;
          color: $white;
          margin: 0;

          @include media-breakpoint-down(md) {
            font-size: $h2-font-size;
          }
        }

        .text {
          font-size: $font-size-md;
          color: $white-1;
          line-height: 1.6;

          @media (max-width: 1399px) {
            max-width: 600px;
            margin: 0 auto;
          }

          @include media-breakpoint-down(md) {
            max-width: 100%;
          }

          @include media-breakpoint-down(sm) {
            font-size: $font-size-sm;
            padding: 0;
          }
        }
      }

      .line {
        position: absolute;
        bottom: -25px;
        left: 47%;
        transform: translateX(-50%);
        z-index: 1;
        display: none;

        @media (min-width: 1400px) {
          display: block;
        }
      }

      .flare {
        position: absolute;
        bottom: -48px;
        left: 424px;
        transform: translateX(-50%);
        z-index: 2;
        display: none;
        width: 50px;
        height: 50px;
        mix-blend-mode: color-dodge;

        @media (min-width: 1400px) {
          display: block;
        }
      }

      .flare-2 {
        position: absolute;
        bottom: 218px;
        left: 55%;
        transform: translateX(-50%);
        z-index: 2;
        display: none;
        width: 50px;
        height: 50px;
        mix-blend-mode: color-dodge;

        @media (min-width: 1400px) {
          display: block;
        }
      }
    }
  }

  .trust {
    min-height: 511px;
    padding: 64px 0;
    background: #0E0F14;
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative;
    border-style: solid;
    border-width: 1px 0;
    border-image: linear-gradient(90deg,
        rgba(71, 68, 80, 0.37) 0%,
        rgba(71, 68, 80, 0.5) 20%,
        rgba(71, 68, 80, 0.2) 50%,
        rgba(71, 68, 80, 0.5) 80%,
        rgba(71, 68, 80, 0.37) 100%) 1;

    &::before {
      content: '';
      position: absolute;
      inset: 50% auto auto 50%;
      transform: translate(-50%, -50%);
      width: 100%;
      height: 564px;
      background:
        linear-gradient(179.47deg, rgba(102, 108, 133, 0) 5.43%, rgba(24, 25, 31, 0.3) 49.42%, rgba(102, 108, 133, 0) 98.04%),
        url('/landing/company/teams/globe.svg') center/contain no-repeat;
      z-index: 1;
      opacity: 0.8;
    }

    .divider {
      position: absolute;
      top: -67px;
      left: 50%;
      transform: translateX(-50%);
      z-index: 10;
      display: flex;
      flex-direction: column;
      align-items: center;

      .logo {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        width: 119.47px;
        height: 109.57px;
        object-fit: contain;
        z-index: 12;
      }
    }

    .container {
      position: relative;
      z-index: 2;
      max-width: 1140px;
      margin: 0 auto;
      padding: 0 20px;

      @include media-breakpoint-up(lg) {
        padding: 0 40px;
      }

      @include media-breakpoint-up(xl) {
        padding: 0 80px;
      }

      @include media-breakpoint-up(xxl) {
        padding: 0 150px;
      }
    }

    .content {
      text-align: center;
      max-width: 800px;
      margin: 0 auto;
      display: flex;
      flex-direction: column;
      gap: 37px;

      .text-white {
        color: $white;
        margin-bottom: 0;
      }

      .title {
        font-weight: 600;
        color: $white;
        padding-top: 2rem;
        margin-bottom: 0;
        line-height: 1.2;

        .gradient {
          background: linear-gradient(89.75deg, #9F79F3 0.22%, #658AF9 99.78%);
          background-clip: text;
          -webkit-background-clip: text;
          -webkit-text-fill-color: transparent;
          color: transparent;
          display: inline-block;
        }
      }

      .text-primary {
        line-height: 1.6;
        margin: 0;
        font-size: $font-size-md;
        font-weight: 400;
        color: $white;

        strong {
          font-weight: 600;
        }
      }

      .text-secondary {
        line-height: 1.6;
        margin: 0;
        font-size: $font-size-md;
        font-weight: 400;
        color: $white-1;

        strong {
          font-weight: 600;
        }
      }

      .logos {
        .grid {
          display: grid;
          width: min(784px, 100%);
          gap: 9.35px;
          place-items: center;
          grid-template-columns: repeat(6, auto);

          @include media-breakpoint-down(lg) {
            grid-template-columns: repeat(3, auto);
            gap: 2.5rem 2rem;
          }

          @include media-breakpoint-down(sm) {
            grid-template-columns: repeat(2, auto);
            gap: 2rem;
          }

          img {
            filter: brightness(0) invert(1);
            object-fit: contain;
          }
        }
      }
    }
  }

  .gradient {
    background: linear-gradient(90.25deg, #7C2EEA 6.26%, #658AF9 53.85%);
    background-clip: text;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    color: transparent;
    display: inline-block;
  }
}
</style>
