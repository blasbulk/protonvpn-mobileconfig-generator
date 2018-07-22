# ProtonVPN Apple Configuration File Generator

This is a self-contained HTML/JavaScript file which generates mobileconfig files containing ProtonVPN-specific IKEv2 VPN settings, for use on Apple iOS and macOS devices. *This project is not affiliated with ProtonVPN in any way.*

## Features

* Client-side processing
* Select multiple VPN servers, and they will all be downloaded and installed as a single mobileconfig file
* Pretty-printed mobileconfig file for easier review

## Instructions

1. You **must** install ProtonVPN's Root CA on your device before you will be able to connect to any ProtonVPN servers. Follow [this link](https://protonvpn.com/download/ProtonVPN_ike_root.der) on the respective device to install the certificate.
1. [Visit this page](https://barracuda6.github.io/protonvpn-mobileconfig-generator/generate.html) using the device you intend to install the mobileconfig file on, **or** download `generate.html` and open it using your web browser, or host it on your own web server.
2. Select the check box next to each server you wish to include in the mobileconfig file.
3. Enter the OpenVPN/IKEv2 username and password found on your [ProtonVPN account settings page](https://account.protonvpn.com/settings) (this is **not** the username and password you normally use to log in!)
4. Configure other settings to your liking.
5. Click on the "Generate" button to download your mobileconfig file.

## Notes

* Use caution when changing "advanced" settings - it is likely that many settings combinations will not work with ProtonVPN.
* Weaker algorithms have been excluded from the generator options.

## Reference

* [Apple Configuration Profile Reference](https://developer.apple.com/enterprise/documentation/Configuration-Profile-Reference.pdf) - Contains additional settings that can be used in mobileconfig files
* [ProtonVPN iOS manual IKEv2 VPN setup](https://protonvpn.com/support/protonvpn-ios-manual-ikev2-vpn-setup/) - ProtonVPN's official instructions on setting up IKEv2 VPNs on iOS devices
