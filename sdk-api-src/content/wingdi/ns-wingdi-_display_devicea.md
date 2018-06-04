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

# _DISPLAY_DEVICEA structure


## -description



The <b>DISPLAY_DEVICE</b> structure receives information about the display device specified by the <i>iDevNum</i> parameter of the <a href="https://msdn.microsoft.com/df3b493c-23d2-4996-9b79-86009efe3078">EnumDisplayDevices</a> function.




## -struct-fields




### -field cb

Size, in bytes, of the <b>DISPLAY_DEVICE</b> structure. This must be initialized prior to calling <a href="https://msdn.microsoft.com/df3b493c-23d2-4996-9b79-86009efe3078">EnumDisplayDevices</a>.


### -field DeviceName

An array of characters identifying the device name. This is either the adapter device or the monitor device.


### -field DeviceString

An array of characters containing the device context string. This is either a description of the display adapter or of the display monitor.


### -field StateFlags

Device state flags. It can be any reasonable combination of the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>DISPLAY_DEVICE_ACTIVE</td>
<td>DISPLAY_DEVICE_ACTIVE specifies whether a monitor is  presented as being "on" by the respective GDI view. <b>Windows Vista:</b> EnumDisplayDevices will only enumerate monitors that can be presented as being "on."

</td>
</tr>
<tr>
<td>DISPLAY_DEVICE_MIRRORING_DRIVER</td>
<td>Represents a pseudo device used to mirror application drawing for remoting or other purposes. An invisible pseudo monitor is associated with this device. For example, NetMeeting uses it. Note that <a href="https://msdn.microsoft.com/d063857b-6036-4e68-80af-9c70d12ae29e">GetSystemMetrics</a> (SM_MONITORS) only accounts for visible display monitors.</td>
</tr>
<tr>
<td>DISPLAY_DEVICE_MODESPRUNED</td>
<td>The device has more display modes than its output devices support.</td>
</tr>
<tr>
<td>DISPLAY_DEVICE_PRIMARY_DEVICE</td>
<td>The primary desktop is on the device. For a system with a single display card, this is always set. For a system with multiple display cards, only one device can have this set.</td>
</tr>
<tr>
<td>DISPLAY_DEVICE_REMOVABLE</td>
<td>The device is removable; it cannot be the primary display.</td>
</tr>
<tr>
<td>DISPLAY_DEVICE_VGA_COMPATIBLE</td>
<td>The device is VGA compatible.</td>
</tr>
</table>
 


### -field DeviceID


            Not used.


### -field DeviceKey

Reserved.


## -remarks



The four string members are set based on the parameters passed to <a href="https://msdn.microsoft.com/df3b493c-23d2-4996-9b79-86009efe3078">EnumDisplayDevices</a>. If the <i>lpDevice</i> param is <b>NULL</b>, then DISPLAY_DEVICE is filled in with information about the display adapter(s). If it is a valid device name, then it is filled in with information about the monitor(s) for that device.




## -see-also




<a href="https://msdn.microsoft.com/0a1023ee-0cab-4978-ad4c-57637379def9">Device Context Structures</a>



<a href="https://msdn.microsoft.com/1fa97368-8931-4687-b37f-ed4db949a150">Device Contexts Overview</a>



<a href="https://msdn.microsoft.com/df3b493c-23d2-4996-9b79-86009efe3078">
        EnumDisplayDevices
      </a>



<a href="https://msdn.microsoft.com/d063857b-6036-4e68-80af-9c70d12ae29e">GetSystemMetrics</a>
 

 

