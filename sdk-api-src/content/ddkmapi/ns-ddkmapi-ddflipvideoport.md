---
UID: NS:ddkmapi._DDFLIPVIDEOPORT
title: DDFLIPVIDEOPORT (ddkmapi.h)
author: windows-sdk-content
description: The DDFLIPVIDEOPORT structure contains the information required to flip the hardware video port.
old-location: display\ddflipvideoport.htm
tech.root: display
ms.assetid: c30c100c-8c91-44e2-b75b-92ce73d44047
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPDDFLIPVIDEOPORT, DDFLIPVIDEOPORT, DDFLIPVIDEOPORT structure [Display Devices], LPDDFLIPVIDEOPORT, LPDDFLIPVIDEOPORT structure pointer [Display Devices], ddkmapi/DDFLIPVIDEOPORT, ddkmapi/LPDDFLIPVIDEOPORT, ddstrcts_b6a3e4ea-217b-40d5-a829-c9ca62632a3e.xml, display.ddflipvideoport"
ms.topic: struct
req.header: ddkmapi.h
req.include-header: Ddkmapi.h
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
 - ddkmapi.h
api_name:
 - DDFLIPVIDEOPORT
product: Windows
targetos: Windows
req.typenames: DDFLIPVIDEOPORT, *LPDDFLIPVIDEOPORT
req.redist: 
---

# DDFLIPVIDEOPORT structure


## -description


The DDFLIPVIDEOPORT structure contains the information required to flip the hardware video port. 


## -struct-fields




### -field hDirectDraw

Specifies the Microsoft DirectDraw handle.


### -field hVideoPort

Specifies the <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">video port extensions (VPE)</a> object handle.


### -field hCurrentSurface

Specifies the current DirectDrawSurface handle.


### -field hTargetSurface

Specifies the handle of the DirectDrawSurface to which the flip occurs.


### -field dwFlags

Indicates whether the surfaces represent <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">VBI</a> surfaces or regular surfaces. One of the following: 

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
Flips the VBI surface.

</td>
</tr>
<tr>
<td>
DDVPFLIP_VIDEO

</td>
<td>
Flips the normal video surface.

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/b6f3a208-2866-4a57-b428-a0dd4ac3b5d4">DD_DXAPI_FLIP_VP</a>



<a href="https://msdn.microsoft.com/c4b38376-b54f-4fbb-b305-5951a1ea76a1">DxApi</a>
 

 

