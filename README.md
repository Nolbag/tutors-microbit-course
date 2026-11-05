# Micro:bit RC Car Workshop

A [Tutors](https://github.com/tutors-sdk/tutors) course that teaches micro:bit coding from scratch and finishes with students programming a radio-controlled car with RFID power-ups. Written for Transition Year students (ages 15-16) on work experience, but it works for any beginner.

Adapted by Paul Nolan and Sophie Hayes from the [original course](https://github.com/rh-outreach-courses/tutors-microbit-course) by Michal Lyra.

## Course outline

| Topic | Labs |
|-------|------|
| 00 Introduction | Meet the micro:bit, the MakeCode editor, downloading code, first program |
| 01 Coding Basics | Events & the LED screen, variables, if/else, loops & functions, challenges |
| 02 Radio Communication | Sender/receiver, tilt remote |
| 03 Robot Car | Joystick remote, car, RFID power-ups, troubleshooting |

## Hardware

- BBC micro:bit (V2 recommended for sound)
- Kitronik :MOVE Motor buggy (car)
- ELECFREAKS Joystick:bit (remote)
- MFRC522 RFID reader and cards (power-ups)

## MakeCode projects

- Finished car with power-ups: https://makecode.microbit.org/S97008-07416-41442-62980
- Finished remote: https://makecode.microbit.org/96640-63492-24223-76730

Both use radio group `10`. Each team must change it to a unique number on **both** devices.

## Publishing

The course is hosted on Netlify. Build settings live in `netlify.toml`, so no manual configuration is needed:

1. Go to https://app.netlify.com/start and import this GitHub repository
2. Pick a site name. It becomes part of the course URL.
3. Deploy. Netlify runs `deno run -A jsr:@tutors/tutors` and publishes the `json` folder.

The course is then available at `https://tutors.dev/course/<netlify-site-name>`. Every push to `main` redeploys it.

## Local preview

```
deno run -A jsr:@tutors/tutors-lite
python3 -m http.server 8080 --directory html
```

Then open http://127.0.0.1:8080.
