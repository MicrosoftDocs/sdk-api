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

# _DDFLIPVIDEOPORTINFO structure


## -description


The DDFLIPVIDEOPORTINFO structure contains the <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">video port extensions (VPE)</a> object and surface information. 


## -struct-fields




### -field lpVideoPortData

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550395">DDVIDEOPORTDATA</a> structure that contains the VPE object information. 


### -field lpCurrentSurface

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550335">DDSURFACEDATA</a> structure that contains information about the current surface. 


### -field lpTargetSurface

Points to a DDSURFACEDATA structure that contains information about the target surface. 


### -field dwFlipVPFlags

Indicates whether the surfaces represent <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">vertical blanking interval (VBI)</a> surfaces or regular surfaces. One of the following: 

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DDVPFLIP_VBI

</td>
<td>
Flip the VBI surface.

</td>
</tr>
<tr>
<td>
DDVPFLIP_VIDEO

</td>
<td>
Flip the normal video surface.

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550335">DDSURFACEDATA</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550395">DDVIDEOPORTDATA</a>



<a href="https://msdn.microsoft.com/d6047c90-1163-475a-a55b-95ccb0570e3e">DxFlipVideoPort</a>
 

 

