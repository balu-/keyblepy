# KeyBLEpy a implementation to control eq3 Smart Locks via Bluetooth

## Current status


Features                           | supported          | tested
---|---|---
Decrypt Message                    |                    |
Encrypt Message                    | :heavy_check_mark: | :heavy_check_mark:
Timeout on operation               | partial            |
discover BLE devices               | :heavy_check_mark: | :heavy_check_mark:
Registering new user               | :heavy_check_mark: | :heavy_check_mark:
Open/Unlock/Lock                   | :heavy_check_mark: | :heavy_check_mark:
Status                             |                    |

## wireshark dissector

The wireshark dissector is written in lua and can be loaded via cmdline

`wireshark -X lua_script:wireshark-evlock.lua`

It has been tested with bluetooth captures from Android (btsnoop\_hci.log).
Enable bluetooth hci snoop log and copy it to your wireshark host.

The dissector supports only unfragmented frames. For encrypted packages only
the message name is shown.
