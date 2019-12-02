
# DNF-Faster, a Patch to DNF for Downloading Packages Faster.

## Requirements:

1. GNU `patch`
2. `aria2c` Downloader
3. `git` (Optional)
You can install both of them by running `sudo dnf install aria2 patch`
    
## How to Patch:
1. Download or Clone this repository: `git clone https://github.com/chitholian/DNF-Faster.git`
2. Enter the new directory: `cd DNF-Faster`
3. Run the patch: `sudo patch -p0 -d/ -b < dnf-faster.patch`
4. Congrats! You got it. You can now do `dnf update`, `dnf upgrade`, `dnf install` etc. `aria2` will download most of the (if not all) target packages using parallel multiconnection.

## How to Undo:
1. Run the command from the `DNF-Faster` directory: `sudo patch -p0 -d/ -b -R < dnf-faster.patch` 
    
## Notes:
1. You need to run the patch each time you `upgrade` the `dnf` package.
2. `DRPM` and `failed` packages will be downloaded by the default `DNF Downloader`.
3. I use this patch because the default dnf downloader is too slow and also makes too much timeout errors.
