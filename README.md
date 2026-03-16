# 功夫茶 Gongfu Brewing Guide

A minimal, offline-capable PWA for gongfu-style tea brewing. Select a tea, follow the steep-by-steep timer, and let the app guide you through each infusion.

## Teas Currently Included

[What-Cha's *'Intro to Tea Collection'*](https://what-cha.com/products/intro-to-tea-collection)

**Green**
- Dragon Well Long Jing
- Obubu Sencha of the Earth

**Oolong**
- Shan Lin Xi Red Oolong
- Four Seasons Oolong
- Amber GABA Oolong

**Black**
- Assam Mancotta SFTGFOP-1
- Ceylon Rosyth Bliss
- Yunnan Golden Tippy
- Mi Xiang Honey Black

## Features

- Steep-by-steep circular timer with audio chime on completion
- Tap any steep indicator to jump forward or back
- Brewing parameters per tea: leaf weight, water temperature, steep count and times
- Works offline after first visit (service worker cached)
- Screen stays awake while a timer is running (Wake Lock API)
- Installable as a standalone app on Android and iOS

## Install on Your Phone

1. Open the hosted URL in Chrome (Android) or Safari (iOS)
2. **Android:** Menu → *Add to Home Screen*
3. **iOS:** Share → *Add to Home Screen*

## Updating the Tea List

All tea data lives in the `TEAS` array near the top of `index.html`. Each tea entry looks like:

```js
{
  name: "Dragon Well 'Long Jing'",
  origin: "China · Zhejiang",
  grams: 5,        // grams per 100ml
  temp: 80,         // water temperature °C
  rinse: false,     // whether to rinse before steeping
  steeps: [15, 20, 25, 30, 40, 50, 65],  // seconds per steep
  notes: "Brewing tips..."
}
```
