---
title: Let's Make Music With a Soil Sensor
seo_title: guide to max for live m4l ableton i2c iic soil sensor music microcontroller mcu esp32 raspberry pi arduino
summary: This is a tutorial on how to use Max for Live to interpret analog data from a soil sensor
description: This is a tutorial on how to use Max for Live to interpret analog data from a soil sensor
slug: soilsensor
author: Tyler Lash

draft: true
date: 2025-01-08T12:51:30-05:00
lastmod: 2025-01-10T12:51:30-05:00
expiryDate: 
publishDate: 

feature_image: cover.png
feature_image_alt: Soil-Sensor

project types: 
    - Audio
    - Electronics
    - Ableton
    - Max for Live

live_url: [youtube link]
source_url: /projects/soilsensor
---

## Overview



## Wiring

Vin to Vin
Gnd to Gnd
Aout to A0


## The Code

10bit adc lets us read data every 10ms without issue
we are sending: 5 bytes every 10ms = 100 packets every second with 8 bits + start/stop bits = 5 * 10 bits * 100 packets = 5000
so 9600 baud is perfect because we are only transferring 5000 bps


## Reading the data in Max for Live

parse, ignore newline bytes, comb for first three bytes
each byte is an ASCII integer value and corresponds to a single digit of a three digit number
let's convert it from integers to ascii
then coll so the ascii values are integers again (atoi will just spit back out the original values)
then music


## Making Noise

theremin if keep as midi inst,
or tie to auto filter with audio effect for pink noise pass