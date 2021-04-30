---
UID: NS:xinput._XINPUT_BATTERY_INFORMATION
title: XINPUT_BATTERY_INFORMATION (xinput.h)
description: Contains information on battery type and charge state.
helpviewer_keywords: ["*PXINPUT_BATTERY_INFORMATION","PXINPUT_BATTERY_INFORMATION","PXINPUT_BATTERY_INFORMATION structure pointer [XInput Game Controller APIs]","XINPUT_BATTERY_INFORMATION","XINPUT_BATTERY_INFORMATION structure [XInput Game Controller APIs]","xinput.xinput_battery_information","xinput/PXINPUT_BATTERY_INFORMATION","xinput/XINPUT_BATTERY_INFORMATION"]
old-location: xinput\xinput_battery_information.htm
tech.root: xinput
ms.assetid: T:Microsoft.directx_sdk.reference.XINPUT_BATTERY_INFORMATION
ms.date: 12/05/2018
ms.keywords: '*PXINPUT_BATTERY_INFORMATION, PXINPUT_BATTERY_INFORMATION, PXINPUT_BATTERY_INFORMATION structure pointer [XInput Game Controller APIs], XINPUT_BATTERY_INFORMATION, XINPUT_BATTERY_INFORMATION structure [XInput Game Controller APIs], xinput.xinput_battery_information, xinput/PXINPUT_BATTERY_INFORMATION, xinput/XINPUT_BATTERY_INFORMATION'
req.header: xinput.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: XINPUT_BATTERY_INFORMATION, *PXINPUT_BATTERY_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _XINPUT_BATTERY_INFORMATION
 - xinput/_XINPUT_BATTERY_INFORMATION
 - PXINPUT_BATTERY_INFORMATION
 - xinput/PXINPUT_BATTERY_INFORMATION
 - XINPUT_BATTERY_INFORMATION
 - xinput/XINPUT_BATTERY_INFORMATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - XInput.h
api_name:
 - XINPUT_BATTERY_INFORMATION
---

# XINPUT_BATTERY_INFORMATION structure


## -description

Contains information on battery type and charge state.

## -struct-fields

### -field BatteryType

The type of battery. <i>BatteryType</i> will be one of the following values.
        

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>BATTERY_TYPE_DISCONNECTED</td>
<td>The device is not connected. </td>
</tr>
<tr>
<td>BATTERY_TYPE_WIRED</td>
<td>The device is a wired device and does not have a battery. </td>
</tr>
<tr>
<td>BATTERY_TYPE_ALKALINE</td>
<td>The device has an alkaline battery. </td>
</tr>
<tr>
<td>BATTERY_TYPE_NIMH</td>
<td>The device has a nickel metal hydride battery. </td>
</tr>
<tr>
<td>BATTERY_TYPE_UNKNOWN</td>
<td>The device has an unknown  battery type. </td>
</tr>
</table>

### -field BatteryLevel

The charge state of the battery. This value is only valid for wireless devices with a known battery type. <i>BatteryLevel</i> will be one of the following values.
        

<table>
<tr>
<th>Value</th>
</tr>
<tr>
<td>BATTERY_LEVEL_EMPTY</td>
</tr>
<tr>
<td>BATTERY_LEVEL_LOW</td>
</tr>
<tr>
<td>BATTERY_LEVEL_MEDIUM</td>
</tr>
<tr>
<td>BATTERY_LEVEL_FULL</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/xinput/ns-xinput-xinput_gamepad">XINPUT_GAMEPAD</a>



<a href="/windows/desktop/xinput/structures">XInput Structures</a>



<a href="/windows/desktop/api/xinput/nf-xinput-xinputgetcapabilities">XInputGetCapabilities</a>



<a href="/windows/desktop/api/xinput/nf-xinput-xinputsetstate">XInputSetState</a>