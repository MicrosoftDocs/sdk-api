---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _XINPUT_BATTERY_INFORMATION structure


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




<a href="https://msdn.microsoft.com/9F3BA764-82E0-4C46-AAA3-F417D2344ECB">XINPUT_GAMEPAD</a>



<a href="https://msdn.microsoft.com/89bb00ea-0be3-9619-1629-a7b7894302d5">XInput Structures</a>



<a href="https://msdn.microsoft.com/5F02EFF5-57ED-4FF1-88E2-DB1CB6F33151">XInputGetCapabilities</a>



<a href="https://msdn.microsoft.com/FA494AEB-9FB9-4AF4-95AB-01048A60D924">XInputSetState</a>
 

 

