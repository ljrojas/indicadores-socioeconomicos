---
title: "Indicadores Socioeconomicos"
author: "Leonardo Rojas"
date: "02-03-2021"
output: 
  html_document:
    keep_md: true
    toc: true
    toc_depth: 4
    toc_float: 
      collapsed: false
      smooth_scroll: false
    
---



# Documentación Calculo de Indicadores Socioeconómicos

El objetivo de este documento es explicar el procesamiento de datos y el cálculo de indicadores socioeconómicos a partir del Censo de Población y Vivienda de 2017 realizado por el INE.

El enfoque es lograr construir cartografías que representen esta información en el territorio nacional.

## Estructura de la información

En esta sección se describen la estructura de la información del censo: tanto la geográfica como la poblacional.

### Información Geográfica

Manzanas y Entidades

Zonas Censales

#### Códigos y división censal

![Fuente: INE 2018](res/img/cod-censo.png)

#### Urbano y Rural

#### Indeterminación Estadística

Indeterminación

Multipolígonos

Referencia: documento ine en docs

### Información poblacional

#### Tabla Personas

#### Tabla Hogares

#### Tabla Vivienda

## Obtención de datos

### Descarga 

Documentación

* Manual de usuario censo: https://redatam-ine.ine.cl/manuales/Manual-Usuario.pdf

* Alcances base cartográfica censal: http://www.censo2017.cl/servicio-de-mapas/descargas/mapas/alcances-base-cartografica-censo2017.pdf



Fuentes de datos

* Manzanas urbanas:

* Entidades rurales:

* Zonas Censales:

* Localidades:

* Microdatos: 

<!--html_preserve--><div id="htmlwidget-03596289e210d1c799bf" style="width:120px;height:480px;" class="grViz html-widget"></div>
<script type="application/json" data-for="htmlwidget-03596289e210d1c799bf">{"x":{"diagram":"digraph {\ngraph [layout = dot, rankdir = BT]\n\na [label = \"Persona\"]\nb [label = \"Hogar\"]\nc [label = \"Vivienda\"]\nd [label = \"Manzana\"]\n\na -> b -> c -> d\n}","config":{"engine":"dot","options":null}},"evals":[],"jsHooks":[]}</script><!--/html_preserve-->


### Paquete Censo2017

## Vinculación de información

Diagrama Proceso Cálculo Indicador:


<!--html_preserve--><div id="htmlwidget-8f35d875e3217bac2908" style="width:672px;height:200px;" class="grViz html-widget"></div>
<script type="application/json" data-for="htmlwidget-8f35d875e3217bac2908">{"x":{"diagram":"digraph {\n\ngraph [layout = dot, rankdir = LR]\n\n# define the global styles of the nodes. We can override these in box if we wish\nnode [shape = rectangle, style = filled, fillcolor = Linen]\n\ndata1 [label = \"Tabla \n Personas\", shape = folder, fillcolor = Beige]\ndata2 [label = \"Polígonos \n Censales\", shape = folder, fillcolor = Beige]\nprocess1 [label =  \"Filtros y \n Agregaciones\"]\nprocess2 [label = \"Vinculación por \n Código Censal\" ]\nind [label = \"Indicador\", fillcolor = Beige]\n\n# edge definitions with the node IDs\n{data1} -> process1\n{data2 process1} -> process2 -> ind\n\n}","config":{"engine":"dot","options":null}},"evals":[],"jsHooks":[]}</script><!--/html_preserve-->

* Agregación información poblacional

* Asociación a código geográfico

* Cartografía

## Indicadores Socioeconómicos

Trabajo sobre zonas censales

### IRH: Indicador de Resilencia de Hogares

Tipos de hogares no monoparentales
<div>
$$ 
\sum_{i=1}^{N} x_i   
$$ 
</div>
### IEJ: Indicador de escolaridad del jefe de hogar

### IPJ: Indicador de Participación Juvenil

Inverso NINI

### IEM: Indicador de Empleo

### ISV: Indicador de Suficiencia de la Vivienda

Hacinamiento

Ojo con vivienda informal

### IVI: Indicador de Calidad de la Vivienda

## Referencias

* INE 2018: Alcances base cartográfica censal: http://www.censo2017.cl/servicio-de-mapas/descargas/mapas/alcances-base-cartografica-censo2017.pdf

* INE 2018: Manual de usuario censo: https://redatam-ine.ine.cl/manuales/Manual-Usuario.pdf

