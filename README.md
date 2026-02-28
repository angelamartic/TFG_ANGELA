# Segmentació semàntica amb U-Net i DeepLabV3 – Dataset LiTS17 

Aquest projecte de TFG té com a objectiu comparar dues arquitectures de segmentació (U-Net i DeepLabV3) aplicades al dataset mèdic **LiTS17**, utilitzant diferents funcions de pèrdua (DiceLoss, IoU).

---

## Estructura de carpetes

### `/Experiments/`
Conté l'entrenament dels models separats per arquitectura i nombre de filtres inicials:

#### `/Experiment001/`

Conté els entrenamentsfets per al métode UNet. A dins d'aquesta capeta trobe dues subcarpetes, una per cada número de filtres.

- '/Experiment001/': Com indica el nom tenim




# Experiment001:

A l'experiment 001 el que estem fent es entrenar el model amb la Red Unet. En quan als resultats, varem fer una primera prova sense canviar les classes de $[0,1,2]$ a $[0,1]$, per veure com funcionava el model, i vam donar a visualitzar la grfica de pérdua i ens varem adonar que la gràfica per al número de filtres $16$ era molt dolenta, en canvi per al número de filtres $32$ era bastant bona. Després varem fer el canvi de classes i varem eliminar la classe $[2]$, i les gràfiques es van intercanviar, és a dir, la grafica del dice loss que apareixia per as números de filtres $16$ ara es la que ens durt en $32$ i igual amb la gràfica de pérdua de $32$ considerant les 3 classes, ara és la que ens surt en $16$ considerant sols les clases $[0,1]$. En tots dos casos, si intentem fer el entrenament amb el el número de filtres en $64$ no ens deixa ja que no hi ha suficient espai.

# Experiment002:

Al'experiment 002 el que estem fent es entrenar el model amb la red DeeplabV3