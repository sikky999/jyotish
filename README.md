
# Jyotish Calculations

A comprehensive JavaScript library for Vedic Astrology (Jyotish) calculations and interpretations.

## Overview

This package provides tools and utilities for performing various Vedic Astrology calculations, including planetary positions, nakshatras (lunar mansions), rashis (zodiac signs), and bhavas (houses). It leverages the Swiss Ephemeris (via the swisseph-v2 package) for precise astronomical calculations.

## Installation

```bash
npm install jyotish-calculations
```

## Features

- **Graha Calculations**: Calculate positions and aspects of the nine planets (grahas) used in Vedic Astrology
- **Nakshatra Determinations**: Calculate and interpret the 27 lunar mansions
- **Rashi Calculations**: Determine zodiac sign positions and interpretations
- **Bhava Analysis**: House system calculations and interpretations
- **Utility Functions**: Helper functions for common Jyotish calculations

## Project Structure

```
jyotish
├── index.js            # Main entry point
├── package.json        # Package configuration
└── src
   ├── bhavas           # House calculations
   ├── grahas           # Planetary calculations
   ├── nakshatras       # Lunar mansion calculations
   ├── rashis           # Zodiac sign calculations
   └── utils            # Helper utilities
```

## Usage

```javascript
const jyotish = require('jyotish-calculations');

// Example: Calculate planet positions for a specific date and location
const date = new Date('1990-01-01T12:00:00Z');
const location = {
  latitude: 28.6139,  // Delhi, India
  longitude: 77.2090,
  altitude: 0
};

const planetPositions = jyotish.grahas.calculatePositions(date, location);
console.log(planetPositions);

// Example: Find the nakshatra of the Moon
const moonNakshatra = jyotish.nakshatras.getNakshatraForPosition(planetPositions.moon.longitude);
console.log(moonNakshatra);
```

## Dependencies

- [swisseph-v2](https://www.npmjs.com/package/swisseph-v2): v1.0.4 - Swiss Ephemeris library for astronomical calculations

## Development

```bash
# Install dependencies
npm install

# Run tests
npm run test:unit
```

## License

ISC

## Contributing

This project is currently under development. Contributions, suggestions, and feedback are welcome.
