# doar - מצא נקודת איסוף קרובה

<p align="center">
  <img src="logo_170x92.png" alt="דואר ישראל" />
</p>

An interactive map to find the nearest Israel Post package pickup point to your address.

**[Live Demo](https://rosenpin.github.io/doar/)**

## The Problem

When Israel Post delivers an international package, you can choose to pick it up from a nearby branch instead of waiting for home delivery. The problem is that [the official website](https://israelpost.co.il) only lets you filter branches **by city** — you pick a city from a dropdown and get a flat list of branches within it.

This is really unhelpful when you're trying to find the **closest** pickup point:

- If you live near a city border, the closest branch might be in a neighboring city — but you'd never see it.
- Within a large city like Tel Aviv (46 branches) or Jerusalem, there's no way to tell which one is actually nearest to you.
- There's no map, no distances, no way to compare — just a dropdown and a list of names.

## The Solution

This project geocodes all **1,424 pickup points** across Israel and plots them on an interactive map. Enter your address, and it instantly shows every branch sorted by distance — across all cities.

**Features:**
- Search by address with autocomplete
- All 1,424 branches on an interactive map
- Sorted by distance from your location (straight line)
- Top 3 closest branches highlighted
- Filter by city
- Mobile responsive

## Tech

- **Leaflet.js** + CartoDB Voyager tiles (Google Maps-like)
- **Nominatim** for address geocoding
- Branch data extracted from the Israel Post website
- Coordinates pre-geocoded via Nominatim + manual lookup for small settlements
- Pure HTML/JS, no build step, no backend
