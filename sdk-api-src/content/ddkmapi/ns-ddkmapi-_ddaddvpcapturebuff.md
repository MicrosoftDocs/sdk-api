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

# _DDADDVPCAPTUREBUFF structure


## -description


The DDADDVPCAPTUREBUFF structure contains the information required to add a new buffer to the internal capture queue. 


## -struct-fields




### -field hCapture

Handle to the <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">video port extensions (VPE)</a> object.


### -field dwFlags

Indicates whether the destination buffer exists in regular system memory or nonlocal display memory (AGP). This member can be one of the following values:

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DDADDBUFF_INVERT

</td>
<td>
The buffer is to be inverted during capture.

</td>
</tr>
<tr>
<td>
DDADDBUFF_NONLOCALVIDMEM

</td>
<td>
The destination buffer exists in nonlocal display memory.

</td>
</tr>
<tr>
<td>
DDADDBUFF_SYSTEMMEMORY

</td>
<td>
The destination buffer exists in system memory.

</td>
</tr>
</table>
 


### -field pMDL

Points to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff554414">MDL</a> (defined in <i>wdm.h</i>) that describes the physical pages of the destination buffer.


### -field pKEvent

Points to a KEVENT that the kernel-mode video transport sets when the destination has been filled.


### -field lpBuffInfo

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff549216">DDCAPBUFFINFO</a> structure that the kernel-mode video transport fills in before setting the KEVENT.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549216">DDCAPBUFFINFO</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550599">DD_DXAPI_ADDVPCAPTUREBUFFER</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff557364">DxApi</a>
 

 

