# Plink

A mesmerizing audio-visual experience that combines generative visual art with Pink Floyd-inspired atmospheric music. Click the canvas to begin a journey through space and sound.

## Features

### Visual Elements
- **Animated ASCII Layer**: Dynamic grid of ASCII characters with breathing effect and shimmering animations
- **Particle System**: 2500 pink particles moving in a spiral pattern with opacity variations
- **Color Palette**: Blue canvas background with orange ASCII characters and pink particles

### Audio Composition
- **Atmospheric Pads**: Long, evolving sawtooth-based chords 
- **Lead Guitar**: Echoey triangle oscillator with delay and reverb 
- **Bassline**: Simple square wave bass with phaser effect 
- **Drums**: Minimal kick, snare, and ride pattern with spacious reverb
- **Wind Atmosphere**: Brown noise with modulated filter for ambient texture
- **Chord Progression**: Dm9 → Gm7 → Cmaj7 → Fmaj7 (repeating)
- **Tempo**: 68 BPM for a dreamy, hypnotic feel

### Audio Effects
- **Reverb**: Long decay (12 seconds) for spacious atmosphere
- **Delay**: Feedback delay for echo effects
- **Phaser**: Modulated phaser for psychedelic textures
- **Dynamic Automation**: Gradual volume swells and parameter modulation

## Technical Implementation

### Technologies Used
- **HTML5 Canvas**: For rendering visual elements
- **Tone.js**: Web Audio framework for music synthesis and sequencing
- **Vanilla JavaScript**: For animation loops and user interaction
- **Tailwind CSS**: For basic styling

### Audio Architecture
```
Instruments → Effects → Master Volume → Output
    ↓
┌─────────┬─────────┬─────────┬─────────┬─────────┐
│   Pad   │  Lead  │  Bass  │  Drums │  Wind  │
└─────────┴─────────┴─────────┴─────────┴─────────┘
    ↓           ↓         ↓         ↓         ↓
┌─────────┐ ┌───────┐ ┌───────┐ ┌───────┐ ┌───────┐
│ Reverb  │ │ Delay │ │ Phaser│ │ Reverb│ │ Filter│
└─────────┘ └───────┘ └───────┘ └───────┘ └───────┘
    ↓           ↓         ↓         ↓         ↓
└───────────────────────────────────────────────┘
                    ↓
              Master Volume
                    ↓
                  Output
```

### Visual Animation Loop
1. Clear canvas with blue background
2. Draw ASCII character layer with breathing effect
3. Update and render particle system
4. Repeat at 60fps

### Audio Sequencing
- Parts are scheduled using Tone.js Transport
- All parts loop seamlessly for continuous playback
- Dynamic automation creates evolving soundscapes

## How to Use

1. **Open the HTML file** in a modern web browser
2. **Click the canvas** to start the audio experience
3. **Enjoy** the mesmerizing combination of visual and audio elements

## Browser Compatibility

- Chrome 60+
- Firefox 55+
- Safari 11+
- Edge 79+

Note: Requires Web Audio API support and user interaction to start audio context.

## Customization

### Visual Customization
- Modify `particleCount` to change number of particles
- Adjust `baseFontSize` to change ASCII character size
- Change colors in the `draw()` function

### Audio Customization
- Adjust BPM in `Tone.Transport.bpm.value`
- Modify chord progression in the `chords` array
- Change instrument parameters in synth definitions
- Adjust effect parameters for different sound character

## Performance Considerations

- Particle count is optimized at 2500 for smooth 60fps animation
- Audio synthesis uses efficient Tone.js scheduling
- ASCII character grid is pre-calculated for performance

## License

MIT License - Feel free to use and modify for your own projects.

## Credits

Inspired by the atmospheric soundscapes of Pink Floyd, particularly the works of:
- David Gilmour (echoey guitar tones)
- Richard Wright (atmospheric keyboards)
- Roger Waters (melodic basslines)
- Nick Mason (spacious drumming)
