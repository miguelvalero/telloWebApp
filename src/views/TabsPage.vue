<template>
  <ion-page>
    <img  :src="presentation" style = "margin-top: 20%;"/>
    <ion-tabs>
      <ion-router-outlet></ion-router-outlet>
      <ion-tab-bar slot="bottom">
        <ion-tab-button tab="OneDroneTab" href='/tabs/OneDrone'>
          <ion-icon :icon="airplaneOutline" />
          <ion-label>One Drone</ion-label>
        </ion-tab-button>
          
        <!-- <ion-tab-button tab="SwarmTab" href='/tabs/Swarm'>
          <ion-icon :icon="appsOutline" />
          <ion-label>Swarm</ion-label>
        </ion-tab-button>
      -->
        
        <ion-tab-button tab="PlayMQTT" href='/tabs/PlayMQTT'>
          <ion-icon :icon="colorWandOutline" />
          <ion-label>Play</ion-label>
        </ion-tab-button>  
        
        <!-- <ion-tab-button tab="PlayWS" href='/tabs/PlayWS'>
          <ion-icon :icon="colorWand" />
          <ion-label>Play</ion-label>
        </ion-tab-button> -->

        <ion-tab-button tab="ShowColor" href='/tabs/ShowColor'>
          <ion-icon :icon="colorFillOutline" />
          <ion-label>Show Color</ion-label>
        </ion-tab-button> 

         <ion-tab-button tab="SetColor" href='/tabs/SetColor'>
          <ion-icon :icon="colorPaletteOutline"/>
          <ion-label>Set Color</ion-label>
        </ion-tab-button>
        <ion-tab-button tab="PlaySpeechMQTT" href='/tabs/PlaySpeechMQTT'>
          <ion-icon :icon="micOutline" />
          <ion-label>Speech</ion-label>
        </ion-tab-button> 
        
      </ion-tab-bar>
    </ion-tabs>
  </ion-page>
</template>

<script>
import { defineComponent } from 'vue';
import { IonTabBar, IonTabButton, IonTabs, IonLabel, IonIcon, IonPage, IonRouterOutlet } from '@ionic/vue';
import { airplaneOutline, appsOutline, colorWandOutline, colorWand, colorPaletteOutline, colorFillOutline , micOutline} from 'ionicons/icons';
import presentation from "./../assets/presentation.png"
export default defineComponent({
  name: 'TabsPage',
  components: { IonLabel, IonTabs, IonTabBar, IonTabButton, IonIcon, IonPage, IonRouterOutlet },
  setup() {
    return {
      airplaneOutline,
      appsOutline,
      colorWandOutline,
      colorWand,
      colorPaletteOutline,
      colorFillOutline,
      micOutline,
      presentation
    }
  }
});
</script>
