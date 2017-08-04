<template>
    <div id="about" style="margin: 40px; background-color: gray">      
      <md-layout>                
        <md-layout style="background-color: brown">f</md-layout>
        <md-layout md-row md-vertical-align="center">
          <md-card md-with-hover>
            <md-card-header>
              <div class="md-title">Title goes here</div>
              <div class="md-subhead">Subtitle here</div>
            </md-card-header>

            <md-card-content>
              Lorem ipsum dolor sit amet, consectetur adipisicing elit. Optio itaque ea, nostrum odio. Dolores, sed accusantium quasi non, voluptas eius illo quas, saepe voluptate pariatur in deleniti minus sint. Excepturi.
            </md-card-content>

            <md-card-actions>
              <md-button>Action</md-button>
              <md-button>Action</md-button>
            </md-card-actions>
          </md-card>
        </md-layout>        
        <md-layout style="background-color: red">f</md-layout>
      </md-layout>      
    </div>
</template>

<style lang="scss" scoped>
  .dialog-fab {
    height: 200px;
  }
</style>

<script>
  export default {
    data: () => ({
      alert: {
        content: 'Your post has been deleted!',
        ok: 'Cool!'
      },
      alert2: {
        title: 'Post created!',
        contentHtml: 'Your post <strong>Material Design is awesome</strong> has been created.'
      },
      confirm: {
        title: 'Use Google\'s location service?',
        contentHtml: 'Let Google help apps determine location. <br> This means sending <strong>anonymous</strong> location data to Google, even when no apps are running.',
        ok: 'Agree',
        cancel: 'Disagree'
      },
      prompt: {
        title: 'What\'s your name?',
        ok: 'Done',
        cancel: 'Cancel',
        id: 'name',
        name: 'name',
        placeholder: 'Type your name...',
        maxlength: 30,
        value: ''
      }
    }),
    methods: {
      openDialog(ref) {
        this.$refs[ref].open()
      },
      closeDialog(ref) {
        this.$refs[ref].close()
      },
      onOpen() {
        console.log('Opened')
      },
      onClose(type) {
        console.log('Closed', type)
      }
    }
  }
</script>
