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

# _DDFLIPOVERLAYINFO structure


## -description


The DDFLIPOVERLAYINFO structure contains the flip information for the surface. 


## -struct-fields




### -field lpCurrentSurface

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550335">DDSURFACEDATA</a> structure that contains information about the current surface. 


### -field lpTargetSurface

Points to a DDSURFACEDATA structure that contains information about the target surface. 


### -field dwFlags

Specifies the polarity of the data in the field being flipped. One of the following flags is returned: 

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DDFLIP_EVEN

</td>
<td>
The target surface contains the even field of video data.

</td>
</tr>
<tr>
<td>
DDFLIP_ODD

</td>
<td>
The target surface contains the odd field of video data.

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550335">DDSURFACEDATA</a>



<a href="https://msdn.microsoft.com/7674f853-e5ea-44c7-b5ed-5fd90bfa1bcb">DxFlipOverlay</a>
 

 

