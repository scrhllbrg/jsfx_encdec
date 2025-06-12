# EncDec Pre/Post EQ and Gain Utility (StudioShoutShoutShout, JSFX)

A JSFX pair for transparent pre/post EQ and gain trimming using shared `gmem` synchronization. Designed for encode/decode-style processing chains, particularly suited for creative compression, transient shaping, and frequency-specific control.

## Features

- Global gain trim with automatic compensation.
- Single-band parametric EQ: Gain, Frequency, Q.
- Parameter synchronisation between pre and post instances via `gmem`.
- Ideal for use with compressors, distortion, saturation, or other processors.

## Parameters

| Control        | Function                         |
|________________|__________________________________|
| Global Gain    | Adjusts pre-input level          |
| EQ Frequency   | 50 Hz – 5 kHz (or entered value) |
| EQ Q           | 0.1 – 10 (narrow to wide)        |
| EQ Gain        | ±30 dB cut/boost                 |

## Usage

1. Insert `shoutshoutshout__enc_dec_pre.jsfx` before your plugin (e.g., compressor).
2. Insert `shoutshoutshout__enc_dec_post.jsfx` after the same plugin.
3. Adjust gain and EQ in the **Pre** instance — the **Post** instance automatically mirrors the settings (inverted where relevant).

## Use cases

- **Reviving a dull snare**  
  A lifeless snare drum can gain energy and presence through frequency-targeted distortion. Insert the **Pre** and **Post** instances of this plugin around a distortion plugin. Use a generous EQ boost with a medium Q in the upper midrange (e.g. 2–5 kHz) to focus the distortion. Works great in parallel with the clean signal.

- **Controlling a loose kick in stereo drum bus**  
  When the kick drum feels too dominant or flappy, insert your favourite compressor between the **Pre** and **Post** instances. Use the Pre-EQ to boost a low frequency (e.g. 50–80 Hz) that aligns with the kick's fundamental. This causes the compressor to respond more aggressively to kick hits — tightening the low end without EQing the final output.

## Installation

Place the `.jsfx` files in your JSFX effects folder. Then restart Reaper.

## License

MIT
