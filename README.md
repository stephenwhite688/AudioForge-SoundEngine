# AudioForge SoundEngine

A realtime .NET audio engine — playback, DSP, codecs, streaming, mixing,
analysis and plugin hosting in one modular set of libraries.

Built to power [MusicForge](https://github.com/stephenwhite688/Music-Forge)
and designed as a standalone SDK for audio applications.

## Packages

| Package | Purpose |
|---|---|
| `AudioForge.SoundEngine` | Facade — realtime playback, DSP chain, meters, EQ, loopback capture |
| `AudioForge.Core` | Core primitives — audio nodes, buffers, device abstractions |
| `AudioForge.Engine` | Engine orchestration across backends, IO and analysis |
| `AudioForge.Backend.Wasapi` | Windows WASAPI output/input backend (via NAudio) |
| `AudioForge.IO` / `AudioForge.IO.Codecs` | Audio file IO and codec decode/encode (WAV, MP3, FLAC, OGG, Opus…) |
| `AudioForge.DSP` | Biquads, convolvers, dynamics, oscillators, analysis primitives |
| `AudioForge.DSP.Spatial` | Spatial audio processing |
| `AudioForge.Effects` | Reverb, delay, modulation effects |
| `AudioForge.Mixing` | Mixing and routing |
| `AudioForge.Analysis` | Loudness (LUFS), true peak, BPM, pitch, replay gain |
| `AudioForge.Streaming` | Network/streaming playback pipeline |
| `AudioForge.MIDI` | MIDI device access and playback |
| `AudioForge.PluginHost` | Managed .NET audio plugin hosting |
| `AudioForge.PluginHost.CLAP` | CLAP native plugin hosting |
| `AudioForge.Visualization` | Realtime spectral/waveform frame production |
| `AudioForge.Visualizer.Contracts` | Contracts for visualiser plugins |

`AudioForge.Benchmarks` and `AudioForge.Verify` are development/verification
tools, not shipped packages.

## Quick start

```csharp
using AudioForge.SoundEngine;

await using var engine = new SoundEngine();
await engine.PlayAsync("track.mp3");
```

See `samples/AudioForge.VisualPlugins.Samples` for a plugin example.

## Requirements

- .NET 10+, Windows (WASAPI backend is Windows-only; core DSP is portable)
- x64 recommended for realtime audio paths

## License

MIT — see [LICENSE](LICENSE).
