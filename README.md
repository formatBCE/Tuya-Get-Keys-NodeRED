# Tuya-Get-Keys-NodeRED

## Why
If you need your device IDs and local keys from Tuya IoT platform (e.g. for usage with localTuya or tuya-local), this NodeRED flow will help you.

## How
0. Get your client ID and client secret from Cloud dashboard on Tuya IoT portal.
1. Import JSON file to your NodeRED flow. 
2. Install needed nodes.
3. In node "Refresh keys" (inject node) put your client ID to corresponding field.
4. In node "Calc Sign" put your client secret to field "Secret Key".
5. Launch subflow with inject node "Refresh keys".
6. Check debug dashboard for messages.

## Where are my keys?
After debug message "Got devices list.", your keys will be stored in flow Context data under "devices" key. You can change this behaviour by editing "Write device info." node. Also, token will be stored there for future updates. If token expires, it will be re-fetched automatically.

Cheers!

[!["Buy Me A Coffee"](https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png)](https://www.buymeacoffee.com/formatbce)
