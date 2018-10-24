---
UID: NS:dxmini._DDFLIPOVERLAYINFO
title: "_DDFLIPOVERLAYINFO"
author: windows-sdk-content
description: The DDFLIPOVERLAYINFO structure contains the flip information for the surface.
old-location: display\ddflipoverlayinfo.htm
tech.root: display
ms.assetid: 04e4baba-4b6c-4f0a-8197-1fb2d83f53d6
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: "*PDDFLIPOVERLAYINFO, DDFLIPOVERLAYINFO, DDFLIPOVERLAYINFO structure [Display Devices], PDDFLIPOVERLAYINFO, PDDFLIPOVERLAYINFO structure pointer [Display Devices], Video_Structs_c9d5aaff-82e8-482e-b774-6c14f0fa8610.xml, _DDFLIPOVERLAYINFO, display.ddflipoverlayinfo, dxmini/DDFLIPOVERLAYINFO, dxmini/PDDFLIPOVERLAYINFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dxmini.h
req.include-header: Dxmini.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxmini.h
api_name:
 - DDFLIPOVERLAYINFO
product: Windows
targetos: Windows
req.typenames: DDFLIPOVERLAYINFO, *PDDFLIPOVERLAYINFO
req.redist: 
---

# _DDFLIPOVERLAYINFO structure


## -description


The DDFLIPOVERLAYINFO structure contains the flip information for the surface. 


## -struct-fields




### -field lpCurrentSurface

Points to a <a href="https://msdn.microsoft.com/4057cfcf-675e-439f-8b51-23adede1d35a">DDSURFACEDATA</a> structure that contains information about the current surface. 


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




<a href="https://msdn.microsoft.com/4057cfcf-675e-439f-8b51-23adede1d35a">DDSURFACEDATA</a>



<a href="https://msdn.microsoft.com/7674f853-e5ea-44c7-b5ed-5fd90bfa1bcb">DxFlipOverlay</a>
 

 

