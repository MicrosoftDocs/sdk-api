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

# _HEAPALIGNMENT structure


## -description


The HEAPALIGNMENT structure contains data specifying the alignment requirements for a given display memory heap. 


## -struct-fields




### -field dwSize

Specifies the size in bytes of this HEAPALIGNMENT structure.


### -field ddsCaps

Specifies a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550286">DDSCAPS</a> structure that indicates what alignment fields are valid. 


### -field dwReserved

Reserved for system use. 


### -field ExecuteBuffer

Specifies a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569895">SURFACEALIGNMENT</a> structure that contains heap alignment requirements for surfaces tagged with DDSCAPS_EXECUTEBUFFER. 


### -field Overlay

Specifies a SURFACEALIGNMENT structure that contains heap alignment requirements for surfaces tagged with DDSCAPS_OVERLAY. 


### -field Texture

Specifies a SURFACEALIGNMENT structure that contains heap alignment requirements for surfaces tagged with DDSCAPS_TEXTURE. 


### -field ZBuffer

Specifies a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569895">SURFACEALIGNMENT</a> structure that contains heap alignment requirements for surfaces tagged with DDSCAPS_ZBUFFER. 


### -field AlphaBuffer

Specifies a SURFACEALIGNMENT structure that contains heap alignment requirements for surfaces tagged with DDSCAPS_ALPHA. 


### -field Offscreen

Specifies a SURFACEALIGNMENT structure that contains heap alignment requirements for surfaces tagged with DDSCAPS_OFFSCREENPLAIN. 


### -field FlipTarget

Specifies a SURFACEALIGNMENT structure that contains heap alignment requirements for surfaces tagged with DDSCAPS_FLIP. 


## -remarks



The driver should verify that the <b>dwSize</b> member is at least as large as <b>sizeof</b>(HEAPALIGNMENT).




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550286">DDSCAPS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569895">SURFACEALIGNMENT</a>
 

 

