# Presentation

[![Circle CI](https://circleci.com/gh/boopathi/presentation.svg?style=svg)](https://circleci.com/gh/boopathi/presentation) ![David DM](https://david-dm.org/boopathi/presentation.svg)

## Why did I build this ?

+ Sometimes, you want the user to copy some text(usually code) while giving your presentation
+ At the same time, you don't want the listener to go ahead of slides and take a look around the final one.

This uses websockets and when the speaker selects the slide from his view, it tells all the connected clients(listeners) to update the slide.

## Overview

### Screencast
https://www.youtube.com/watch?v=nuuneB5u9xk

```
+-----------------------------------+
|                                   |
|               SPEAKER             |
|     http://localhost/controller   |
|                                   |
+--+----+----+----+----+----+----+--+
   |    |    |    |    |    |    |   
   |websocket.emit('change_slide')   
   |    |    |    |    |    |    |   
 +-v+ +-v+ +-v+ +-v+ +-v+ +-v+ +-v+  
 |1 | |2 | |3 | |4 | |5 | |6 | |7 |  
 +--+ +--+ +--+ +--+ +--+ +--+ +--+  
                                     
         CLIENTS / LISTENERS         
         http://speaker_host/          

```

## Installation

+ `npm install`
+ `webpack`
+ `npm start`

## Usage

+ Presenter View - "http://localhost:4242/controller" - Add, Edit, Remove, Present slides
+ Listener View - "http://localhost:4242/" - View slides

## TODO

(Work in Progress)

Doesn't work now. Still building this feature.

+ `npm install -g presentation`
+ `presentation ./my-presentation.md`
