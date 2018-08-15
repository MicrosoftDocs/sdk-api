---
UID: NS:xinput._XINPUT_BATTERY_INFORMATION
title: "_XINPUT_BATTERY_INFORMATION"
author: windows-sdk-content
description: Contains information on battery type and charge state.
old-location: xinput\xinput_battery_information.htm
old-project: xinput
ms.assetid: T:Microsoft.directx_sdk.reference.XINPUT_BATTERY_INFORMATION
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: "*PXINPUT_BATTERY_INFORMATION, PXINPUT_BATTERY_INFORMATION, PXINPUT_BATTERY_INFORMATION structure pointer [XInput Game Controller APIs], XINPUT_BATTERY_INFORMATION, XINPUT_BATTERY_INFORMATION structure [XInput Game Controller APIs], _XINPUT_BATTERY_INFORMATION, xinput.xinput_battery_information, xinput/PXINPUT_BATTERY_INFORMATION, xinput/XINPUT_BATTERY_INFORMATION"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: xinput.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: XINPUT_BATTERY_INFORMATION, *PXINPUT_BATTERY_INFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - XInput.h
api_name:
 - XINPUT_BATTERY_INFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
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




<a href="https://msdn.microsoft.com/en-us/library/Ee419270(v=VS.85).aspx">XINPUT_GAMEPAD</a>



<a href="https://msdn.microsoft.com/89bb00ea-0be3-9619-1629-a7b7894302d5">XInput Structures</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee419264(v=VS.85).aspx">XInputGetCapabilities</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee419268(v=VS.85).aspx">XInputSetState</a>
 

 

