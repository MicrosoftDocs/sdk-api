---
UID: NS:dxmini._DDFLIPVIDEOPORTINFO
title: "_DDFLIPVIDEOPORTINFO"
author: windows-sdk-content
description: The DDFLIPVIDEOPORTINFO structure contains the video port extensions (VPE) object and surface information.
old-location: display\ddflipvideoportinfo.htm
old-project: display
ms.assetid: 9cf87d19-2db6-48f8-96a6-2b6ac969c774
ms.author: windowssdkdev
ms.date: 08/13/2018
ms.keywords: "*PDDFLIPVIDEOPORTINFO, DDFLIPVIDEOPORTINFO, DDFLIPVIDEOPORTINFO structure [Display Devices], PDDFLIPVIDEOPORTINFO, PDDFLIPVIDEOPORTINFO structure pointer [Display Devices], Video_Structs_e5e5e93f-25a2-47a6-a99c-6ac8ca43f069.xml, _DDFLIPVIDEOPORTINFO, display.ddflipvideoportinfo, dxmini/DDFLIPVIDEOPORTINFO, dxmini/PDDFLIPVIDEOPORTINFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dxmini.h
req.include-header: Dxmini.h
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
req.typenames: DDFLIPVIDEOPORTINFO, *PDDFLIPVIDEOPORTINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxmini.h
api_name:
 - DDFLIPVIDEOPORTINFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _DDFLIPVIDEOPORTINFO structure


## -description


The DDFLIPVIDEOPORTINFO structure contains the <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">video port extensions (VPE)</a> object and surface information. 


## -struct-fields




### -field lpVideoPortData

Points to a <a href="https://msdn.microsoft.com/662ff6ee-d6b1-4cb1-8ff8-b4c1e17b26df">DDVIDEOPORTDATA</a> structure that contains the VPE object information. 


### -field lpCurrentSurface

Points to a <a href="https://msdn.microsoft.com/4057cfcf-675e-439f-8b51-23adede1d35a">DDSURFACEDATA</a> structure that contains information about the current surface. 


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




<a href="https://msdn.microsoft.com/4057cfcf-675e-439f-8b51-23adede1d35a">DDSURFACEDATA</a>



<a href="https://msdn.microsoft.com/662ff6ee-d6b1-4cb1-8ff8-b4c1e17b26df">DDVIDEOPORTDATA</a>



<a href="https://msdn.microsoft.com/d6047c90-1163-475a-a55b-95ccb0570e3e">DxFlipVideoPort</a>
 

 

