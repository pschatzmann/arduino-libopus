# libopus for Arduino

Opus is a codec for interactive speech and audio transmission over the Internet.

Opus can handle a wide range of interactive audio applications, including
Voice over IP, videoconferencing, in-game  chat, and even remote live music
performances. It can scale from low bit-rate narrowband speech to very high
quality stereo music.

Opus, when coupled with an appropriate container format, is also suitable
for non-realtime  stored-file applications such as music distribution, game
soundtracks, portable music players, jukeboxes, and other applications that
have historically used high latency formats such as MP3, AAC, or Vorbis.

                    Opus is specified by IETF RFC 6716:
                    https://tools.ietf.org/html/rfc6716

The Opus format and this implementation of it are subject to the royalty-
free patent and copyright licenses specified in the file COPYING.

Opus packets are not self-delimiting, but are designed to be used inside a __container__ of some sort which supplies the decoder with each packet's length. Opus was originally specified for encapsulation in __Ogg containers__.

This project contains

- [the opus codec](https://opus-codec.org/)
- [libogg](https://xiph.org/ogg/)
- [liboggz](https://www.xiph.org/oggz/)


## Installation in Arduino

You can download the library as zip and call include Library -> zip library. Or you can git clone this project into the Arduino libraries folder e.g. with

```
cd  ~/Documents/Arduino/libraries
git clone https://github.com/pschatzmann/arduino-libopus.git

```

## Design

In order to create an Arduino compatible library I executed the following steps:

- Added the projects to the src directory
- Symlinked the header files into src
- Symlinked additional header subdirectories
- Moved offending code which was platform specific or contained a main() to the removed directory
- Added a config.h to the src directory and to src/liboggz

