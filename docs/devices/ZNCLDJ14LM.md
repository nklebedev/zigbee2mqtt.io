---
title: "Aqara ZNCLDJ14LM control via MQTT"
description: "Integrate your Aqara ZNCLDJ14LM via Zigbee2MQTT with whatever smart home infrastructure you are using without the vendor's bridge or gateway."
addedAt: 2023-01-01T08:59:10
pageClass: device-page
---

<!-- !!!! -->
<!-- ATTENTION: This file is auto-generated through docgen! -->
<!-- You can only edit the "Notes"-Section between the two comment lines "Notes BEGIN" and "Notes END". -->
<!-- Do not use h1 or h2 heading within "## Notes"-Section. -->
<!-- !!!! -->

# Aqara ZNCLDJ14LM

|     |     |
|-----|-----|
| Model | ZNCLDJ14LM  |
| Vendor  | [Aqara](/supported-devices/#v=Aqara)  |
| Description | Curtain controller C2 |
| Exposes | cover (state, position), running, motor_state, power_outage_count, linkquality |
| Picture | ![Aqara ZNCLDJ14LM](https://www.zigbee2mqtt.io/images/devices/ZNCLDJ14LM.jpg) |


<!-- Notes BEGIN: You can edit here. Add "## Notes" headline if not already present. -->


<!-- Notes END: Do not edit below this line -->


## OTA updates
This device supports OTA updates, for more information see [OTA updates](../guide/usage/ota_updates.md).


## Options
*[How to use device type specific configuration](../guide/configuration/devices-groups.md#specific-device-options)*

* `invert_cover`: Inverts the cover position, false: open=100,close=0, true: open=0,close=100 (default false). The value must be `true` or `false`


## Exposes

### Cover 
The current state of this cover is in the published state under the `state` property (value is `OPEN` or `CLOSE`).
To control this cover publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"state": "OPEN"}`, `{"state": "CLOSE"}`, `{"state": "STOP"}`.
To read the current state of this cover publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/get` with payload `{"state": ""}`.
To change the position publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"position": VALUE}` where `VALUE` is a number between `0` and `100`.

### Running (binary)
Whether the motor is moving or not.
Value can be found in the published state on the `running` property.
It's not possible to read (`/get`) or write (`/set`) this value.
If value equals `true` running is ON, if `false` OFF.

### Motor state (enum)
The current state of the motor..
Value can be found in the published state on the `motor_state` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The possible values are: `closing`, `opening`, `stop`.

### Power outage count (numeric)
Number of power outages (since last pairing).
Value can be found in the published state on the `power_outage_count` property.
It's not possible to read (`/get`) or write (`/set`) this value.

### Linkquality (numeric)
Link quality (signal strength).
Value can be found in the published state on the `linkquality` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The minimal value is `0` and the maximum value is `255`.
The unit of this value is `lqi`.

