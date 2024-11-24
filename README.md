# Fix for scarlett solo
If your microphone level is low using the scarlett's official drivers, you can use this.
Just uninstall the focusrite driver for the scarlett and restart your computer.
Now the level should be a lot higher but only for left channel. This app duplicates the left channel to the right and outputs it in virtual-audio cable.

# What it do?

While running, cli app will duplicate your microphone's left channel into a virtual audio cable.
You can then just select virtual audio cable's output as your default microphone.
ctrl-c to stop the script.

# Install
```shell
cargo build --release
```
```shell
cargo run --release -- -l 30 -i "Microphone (Scarlett Solo USB)" -o "CABLE Input (VB-Audio Virtual Cable)"
```

# Credits
Thanks to the cpal's project amazing example which was slightly modified to duplicate the left channel.