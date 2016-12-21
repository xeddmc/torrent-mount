# torrent-mount

Mount a torrent (or magnet link) as a filesystem in real time using [torrent-stream](https://github.com/mafintosh/torrent-stream) and fuse.


```
npm install -g torrent-mount
```

You also need to install fuse. See [this link](https://github.com/mafintosh/fuse-bindings#requirements) for more info.

## Usage

Open a terminal and cd to a directory where you want to mount your torrent

```
torrent-mount magnet:?xt=urn:btih:ef330b39f4801d25b4245212e75a38634bfc856e
```
```
Usage: torrent-mount <source>... [options]

source     .torrent file or magnet link to open

Options:
	-m PATH, --mount PATH   Mount location path [directory]  [.]
	-l, --lazy              Download only if accessed
```

After doing that open the same directory using a file browser.
The files of the torrent should be mounted there now and you should be able to double-click them to start streaming as regular files!


## Troubleshooting

Download the latest osxfuse `dmg` using this link and install it

https://github.com/osxfuse/osxfuse/releases/latest

You also need pkg-config:

```
brew install pkg-config
```

## License

MIT
