<template>
  <ion-page>
    <ion-header :translucent="true">
      <ion-toolbar>
        <ion-title>Blank</ion-title>
      </ion-toolbar>
    </ion-header>

    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Vue Ionic 測試</ion-title>
        </ion-toolbar>
      </ion-header>

      <div id="container">
        <ion-card>
          <ion-item href="#" class="ion-activated">
            <ion-icon :icon="wifi" slot="start"></ion-icon>
            <ion-label>Card Link Item 1 activated</ion-label>
          </ion-item>

          <ion-item href="#">
            <ion-icon :icon="wine" slot="start"></ion-icon>
            <ion-label>Card Link Item 2</ion-label>
          </ion-item>

          <ion-item class="ion-activated">
            <ion-icon :icon="warning" slot="start"></ion-icon>
            <ion-label>Card Button Item 1 activated</ion-label>
          </ion-item>

          <ion-item>
            <ion-icon :icon="walk" slot="start"></ion-icon>
            <ion-label>Card Button Item 2</ion-label>
          </ion-item>
        </ion-card>
        <strong>Ready to create an app?</strong>
        <p>Start with Ionic <a target="_blank" rel="noopener noreferrer" href="https://ionicframework.com/docs/components">UI Components</a></p>
        <ion-button color="light">test</ion-button>
      </div>
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { IonCard, IonIcon, IonItem, IonLabel } from '@ionic/vue';
import { IonButton } from '@ionic/vue';
import { IonContent, IonHeader, IonPage, IonTitle, IonToolbar } from '@ionic/vue';
import { wine, walk, warning, wifi } from 'ionicons/icons';
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'Home',
  components: {
    IonContent,
    IonHeader,
    IonPage,
    IonTitle,
    IonToolbar,
    IonButton,
    IonCard, IonIcon, IonItem, IonLabel
  },
  setup () {
    return {
      warning,
      wifi,
      wine,
      walk
    };
  }
});
</script>

<style scoped>
#container {
  text-align: center;

  position: absolute;
  left: 0;
  right: 0;
  top: 50%;
  transform: translateY(-50%);
}

#container strong {
  font-size: 20px;
  line-height: 26px;
}

#container p {
  font-size: 16px;
  line-height: 22px;

  color: #8c8c8c;

  margin: 0;
}

#container a {
  text-decoration: none;
}
</style>