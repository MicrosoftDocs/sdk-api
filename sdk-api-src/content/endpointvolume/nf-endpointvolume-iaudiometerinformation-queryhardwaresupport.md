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

# IAudioMeterInformation::QueryHardwareSupport


## -description



The <b>QueryHardwareSupport</b> method queries the audio endpoint device for its hardware-supported functions.




## -parameters




### -param pdwHardwareSupportMask [out]

Pointer to a <b>DWORD</b> variable into which the method writes a hardware support mask that indicates the hardware capabilities of the audio endpoint device. The method can set the mask to 0 or to the bitwise-OR combination of one or more <a href="https://msdn.microsoft.com/54032f75-2287-4589-bda5-e005ee077c41">ENDPOINT_HARDWARE_SUPPORT_XXX</a> constants.


## -returns



If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>pdwHardwareSupportMask</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



This method indicates whether the audio endpoint device implements the following functions in hardware:

<ul>
<li>Volume control</li>
<li>Mute control</li>
<li>Peak meter</li>
</ul>
The system automatically substitutes a software implementation for any function in the preceding list that the endpoint devices does not implement in hardware.




## -see-also




<a href="https://msdn.microsoft.com/eff1c1cd-792b-489a-8381-4b783c57f005">IAudioMeterInformation Interface</a>
 

 

