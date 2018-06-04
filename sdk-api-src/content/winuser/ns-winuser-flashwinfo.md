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

# FLASHWINFO structure


## -description


Contains the flash status for a window and the number of times the system should flash the window.


## -struct-fields




### -field cbSize

The size of the structure, in bytes.


### -field hwnd

A handle to the window to be flashed. The window can be either opened or minimized.


### -field dwFlags

The flash status. This parameter can be one or more of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FLASHW_ALL"></a><a id="flashw_all"></a><dl>
<dt><b>FLASHW_ALL</b></dt>
<dt>0x00000003</dt>
</dl>
</td>
<td width="60%">
Flash both the window caption and taskbar button. This is equivalent to setting the FLASHW_CAPTION | FLASHW_TRAY flags.

</td>
</tr>
<tr>
<td width="40%"><a id="FLASHW_CAPTION"></a><a id="flashw_caption"></a><dl>
<dt><b>FLASHW_CAPTION</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Flash the window caption.

</td>
</tr>
<tr>
<td width="40%"><a id="FLASHW_STOP"></a><a id="flashw_stop"></a><dl>
<dt><b>FLASHW_STOP</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Stop flashing. The system restores the window to its original state.

</td>
</tr>
<tr>
<td width="40%"><a id="FLASHW_TIMER"></a><a id="flashw_timer"></a><dl>
<dt><b>FLASHW_TIMER</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Flash continuously, until the FLASHW_STOP flag is set.

</td>
</tr>
<tr>
<td width="40%"><a id="FLASHW_TIMERNOFG"></a><a id="flashw_timernofg"></a><dl>
<dt><b>FLASHW_TIMERNOFG</b></dt>
<dt>0x0000000C</dt>
</dl>
</td>
<td width="60%">
Flash continuously until the window comes to the foreground.

</td>
</tr>
<tr>
<td width="40%"><a id="FLASHW_TRAY"></a><a id="flashw_tray"></a><dl>
<dt><b>FLASHW_TRAY</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Flash the taskbar button.

</td>
</tr>
</table>
 


### -field uCount

The number of times to flash the window.


### -field dwTimeout

The rate at which the window is to be flashed, in milliseconds. If <b>dwTimeout</b> is zero, the function uses the default cursor blink rate.


## -see-also




<a href="https://msdn.microsoft.com/474ec2d9-3ee9-4622-843e-d6ae36fedd7f">FlashWindowEx</a>
 

 

