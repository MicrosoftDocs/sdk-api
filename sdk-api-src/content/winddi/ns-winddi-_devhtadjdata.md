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

# _DEVHTADJDATA structure


## -description


The DEVHTADJDATA structure is used as input to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff567308">HTUI_DeviceColorAdjustment</a> function.


## -struct-fields




### -field DeviceFlags

Is a set of flags, set by the caller, describing color mixing and color versus gray-scale output. Either, both, or neither of the following flags should be set, as appropriate:

<table>
<tr>
<th>Flag</th>
<th>Definition</th>
</tr>
<tr>
<td>
DEVHTADJF_ADDITIVE_DEVICE

</td>
<td>

<dl>
<dt>If set, the device uses additive color mixing.</dt>
<dt>If not set, the device uses subtractive color mixing.</dt>
</dl>


</td>
</tr>
<tr>
<td>
DEVHTADJF_COLOR_DEVICE

</td>
<td>

<dl>
<dt>If set, the device produces color output.</dt>
<dt>If not set, the device produces gray-scaled output.</dt>
</dl>


</td>
</tr>
</table>
 


### -field DeviceXDPI

Is the caller-supplied horizontal resolution, in dots per inch, for the device.


### -field DeviceYDPI

Is the caller-supplied vertical resolution, in dots per inch, for the device.


### -field pDefHTInfo

Is a caller-supplied pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff552833">DEVHTINFO</a> structure containing the device's default halftoning properties.


### -field pAdjHTInfo

Is a caller-supplied pointer to a DEVHTINFO structure containing the device's current halftoning properties. Before the <a href="https://msdn.microsoft.com/library/windows/hardware/ff567308">HTUI_DeviceColorAdjustment</a> function returns, it modifies this structure's contents, if the user has adjusted the halftoning properties. Can be <b>NULL</b> (see the following Remarks section).


## -remarks



If <b>pAdjHTInfo</b> is <b>NULL</b>, or if <b>pAdjHTInfo</b> and <b>pDefHTInfo</b> point to the same buffer, the <a href="https://msdn.microsoft.com/library/windows/hardware/ff567308">HTUI_DeviceColorAdjustment</a> function displays the halftoning properties supplied by <b>pDefHTInfo</b> but does not allow the user to modify them.



