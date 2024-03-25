
# Aseprite Builder

[![GitHub license](https://img.shields.io/github/license/symartin/aseprite_builder.svg)](https://raw.githubusercontent.com/symartin/aseprite_builder/main/LICENSE)

## What is it
Automated workflow for GitHub Actions which builds Aseprite for Windows and linux forked from [ellisonoswalt/aseprite_builder](https://github.com/ellisonoswalt/aseprite_builder) repository with some cherypicking from [sallandcall/aseprite_builder](https://github.com/sallandcall/aseprite_builder) and [ilobilo/aseprite_builder](https://github.com/ilobilo/aseprite_builder) updated scripts.

By using GitHub actions there is no need for manual compilation and it does not contain malware. To adhere to the EULA of Aseprite, this workflow does not upload the binary in a public accessible space like artifacts. The release can be found within the releases as a draft (only visible for repo owner).

## How to use
1. Clone or fork this repo
2. Go to Action
3. Select Build and deploy Aseprite - Windows
4. click on Run workfow > Run workfow (see [Github doc](https://docs.github.com/en/actions/using-workflows/manually-running-a-workflow) for more details)
5. The C.I. will run and create a "draft" release 

To use the binary, one need `libcrypto-1_1-x64.dll`. It can be download from [overbyte.eu](https://wiki.overbyte.eu/wiki/index.php/ICS_Download#Download_OpenSSL_Binaries) under OpenSSL Binaries Win-64 1.1.x and copy in the exe folder.

## Technical details
This workflow follows the instructions as described at [Aseprite repo](https://github.com/aseprite/aseprite/blob/master/INSTALL.md)

## Build times
Every month you have 2000 free minutes from GitHub.</br>
Different Operating Systems costs different amounts of minutes, see [billing for GitHub Actions](https://help.github.com/en/github/setting-up-and-managing-billing-and-payments-on-github/about-billing-for-github-actions#about-billing-for-github-actions)</br>
So building for all three Operating Systems will cost 130 minutes (20 * 2+10 * 1+8 * 10)</br>
That is why we recommend you to modify the **os** line to only build for the OS that you need.
|Operating System|Minutes|Minute multiplier
|---|---|---|
|Windows|20|2|
|Ubuntu|10|1|
|macOS|8|10|

## Support Aseprite
Keep supporting Aseprite at https://aseprite.org/#buy
