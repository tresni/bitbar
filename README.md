# ![BitBar](https://github.com/matryer/bitbar/raw/master/Docs/bitbar-32.png) BitBar

BitBar (by [Mat Ryer - @matryer](https://twitter.com/matryer)) lets you put the output from any script/program in your Mac OS X Menu Bar.

  * [Download](https://github.com/matryer/bitbar/releases) and [View plugin repository](https://github.com/matryer/bitbar-plugins)
  * [Get started](#get-started)
  * [Installing plugins](#installing-plugins)
  * [Contributing](#contributing)
  * [Thanks](#thanks)

Example showing the latest Buy and Sell figures for BitCoins:

![BitBar Example showing BitCoins plugin](https://raw.github.com/matryer/bitbar/master/Docs/BitBar-Example-Bitcoins.png)

Click to see the full output, and more options:

![BitBar Example showing menu open](https://raw.github.com/matryer/bitbar/master/Docs/BitBar-Example-Menu.png)

Example showing your internal and external IP addresses:

![BitBar Example showing IP Addresses](https://raw.github.com/matryer/bitbar/master/Docs/BitBar-Example-IPs.png)

## Get started

[Get the latest version of BitBar](https://github.com/matryer/bitbar/releases). Copy it to your Applications folder and run it - it will ask you to (create and) elect a plugins folder, do so.

Homebrew Cask users can, alternatively, install BitBar by running `brew cask install bitbar`.

[Browse our plugins](https://github.com/matryer/bitbar-plugins) to find useful scripts, or [write your own](https://github.com/matryer/bitbar-plugins#write-your-own)

### It's free, so please donate

If you love this, any BitCoin donations are most welcome, to `1DGoNEYAnjE5DqK7y5zMPR4PLU5HLKpLNR` or [send something useful (Amazon Wishlist)](http://amzn.to/1Pd9yOt).

## Installing plugins

Just download the plugin of your choice into your BitBar plugins directory and choose 'Reset' from one of the BitBar menus. 

### Configure the refresh time

The refresh time is in the filename of the plugin, following this format:

    {name}.{time}.{ext}

  * `name` - The name of the file
  * `time` - The refresh rate (see below)
  * `ext` - The file extension

For example:

  * `date.1m.sh` would refresh every minute.

Most plugins will come with a default, but you can change it to anything you like:

  * 10s - ten seconds
  * 1m - one minute
  * 2h - two hours
  * 1d - a day

### Ensure you have execution rights

Ensure the plugin is executable by running `chmod +x plugin.sh`.

### Using symlinks

Because Git will ignore everything in `Plugins/Enabled`, you can use it to maintain your own plugins directory while still benefitting from tracking (upstream) changes.

#### Example

	cd Plugins/Enabled
	
	# Enable spotify plugin
	ln -s ../Music/spotify.10s.sh
	
	# Enable uptime plugin and change update interval to 30 seconds
	ln -s ../System/uptime.1m.sh uptime.30s.sh
	
Then select the `Enabled` folder in your BitBar preferences.

#### Resetting Plugin Directory

In case you made the mistake of choosing a directory with thousands of files as the plugin directory and BitBar getting stuck forever, do this from terminal to reset it:

`defaults delete com.matryer.BitBar`

## Contributing

  * If you want to contribute a plugin, please head over to the [Plugin repository](https://github.com/matryer/bitbar-plugins#write-your-own) and submit a pull request

### BitBar app

To work on the BitBar app, fork, then clone this repo.

In terminal, navigate to the project directory and run:

```
git submodule init && git submodule update
```

## Thanks

  * Special thanks to [@muhqu](https://github.com/muhqu) and [@tylerb](https://github.com/tylerb) for all their help (see commit history for details)
  * Thanks to [Chris Ryer](http://www.chrisryer.co.uk/) for the app logo - and to [@mazondo](https://twitter.com/mazondo) for the original
  * Thanks for all our [plugin contributors](https://github.com/matryer/bitbar-plugins) who have come up with some pretty genius things
