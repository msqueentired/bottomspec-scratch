# Bottom-Scratch

Bottom-Scratch is a partial implementation of the [Bottom Specification](https://github.com/bottom-software-foundation/spec) in Scratch 3.0. Right now, decoding is not implemented.

```
💖✨✨✨,,,👉👈💖✨✨✨✨🥺,,,,👉👈💖💖✨,,,,👉👈💖✨✨✨✨🥺,,👉👈💖💖✨🥺,👉👈💖✨✨✨✨🥺,,,,👉👈💖💖,,,,👉👈✨✨✨,,👉👈💖💖🥺,,,,👉👈💖💖,👉👈💖✨,,,👉👈✨✨✨,,👉👈🫂✨✨✨✨👉👈💖💖💖🥺,,,,👉👈💖💖💖,,👉👈💖💖💖✨✨🥺,,,,👉👈✨✨✨,,👉👈🫂✨✨✨✨👉👈💖💖💖🥺,,,,👉👈💖💖💖,,👉👈💖💖💖✨✨🥺,,,,👉👈✨✨✨,,👉👈💖✨✨✨👉👈💖💖🥺,,,👉👈💖💖✨🥺👉👈💖✨,,,👉👈💖✨,,,👉👈💖✨,,,👉👈💖✨,,,👉👈
```

## Usage

Open `bottom_scratch.sb3` in Scratch 3.0. Press the green flag, type your text into the input box, and hit return.

## Limitations

* Scratch has no way to encode UTF-8 because it is made for children, and children are not legally allowed to think about Unicode.

  * As such, decimal conversions are handled by creating a lookup table of characters and doing some math to turn their position into the appropriate decimal representation.

* The editor refuses to open this project if I try to include any more than the first two blocks of the Basic Multilingual Plane (`0000` to `00FF`). I'm not sure if lists max out at 256 characters or if it's a limitation on project size.


* Currently the encoded text is displayed in the speech bubble, which has a limit of 128 characters.

## Contributing

Pull requests are welcome, just create an issue first.

### Notes on contributing

Scratch "binaries" (`smb3`) are just regular `ZIP` files with the extension changed, and all actual project data is stored as a `JSON` file within it. A decompressed version of the project can be found in `bottom_scratch.sb3_FILES/`. While modifying the code can (and should) be done through the IDE, lookup tables must be modified by editing `project.json` directly. Scratch's import/export function can't handle large amounts of data.


### Why would you do this?

I am filled with sin.

## License

Bottom-Scratch is released under the [MIT License](license.md).

#### This project is in neither affiliated with nor endorsed by the Scratch Foundation or Lifelong Kindergarten Group at MIT Media Lab.
