<template>
  <div class="education">
    <SectionHeading heading="Education &amp; Certification" />
    <div
      v-for="certificate in certificates"
      :key="certificate.title"
      class="u-padding-tb-lg"
    >
      <h3 class="education__title">{{ certificate.title }}</h3>
      <span>({{ certificate.from }} - {{ certificate.to }})</span>
      <p class="education__issuer">{{ certificate.issuer }}</p>
    </div>
  </div>
</template>

<script>
import SectionHeading from './sectionHeading'

export default {
  name: 'Education',
  components: {
    SectionHeading,
  },
  data() {
    const be = {
      title: 'Bachelor of Engineering in Information Science',
      issuer: 'Visvesvaraya Technological University',
      from: 'August 2012',
      to: 'June 2016'
    }
    const devAssociate = {
      title: 'AWS Certified Developer - Associate (DVA-C01)',
      issuer: 'AWS Training and Certification',
      from: 'October 2019',
      to: 'October 2022'
    }
    const certificates = [ be, devAssociate ]
    return { certificates }
  },
}
</script>
