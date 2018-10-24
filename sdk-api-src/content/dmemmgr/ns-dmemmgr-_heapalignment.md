---
UID: NS:dmemmgr._HEAPALIGNMENT
title: "_HEAPALIGNMENT"
author: windows-sdk-content
description: The HEAPALIGNMENT structure contains data specifying the alignment requirements for a given display memory heap.
old-location: display\heapalignment.htm
tech.root: display
ms.assetid: 546029c7-c92e-4940-841f-235c7dc50e8e
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: "*LPHEAPALIGNMENT, HEAPALIGNMENT, HEAPALIGNMENT structure [Display Devices], _HEAPALIGNMENT, ddstrcts_ec77ce92-8153-4be6-8720-f8070efce79a.xml, display.heapalignment, dmemmgr/HEAPALIGNMENT"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dmemmgr.h
req.include-header: Dmemmgr.h
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
 - dmemmgr.h
api_name:
 - HEAPALIGNMENT
product: Windows
targetos: Windows
req.typenames: HEAPALIGNMENT, *LPHEAPALIGNMENT
req.redist: 
---

# _HEAPALIGNMENT structure


## -description


The HEAPALIGNMENT structure contains data specifying the alignment requirements for a given display memory heap. 


## -struct-fields




### -field dwSize

Specifies the size in bytes of this HEAPALIGNMENT structure.


### -field ddsCaps

Specifies a <a href="https://msdn.microsoft.com/e1ed1fa2-2f3c-4d04-a601-c11fb77eb5cc">DDSCAPS</a> structure that indicates what alignment fields are valid. 


### -field dwReserved

Reserved for system use. 


### -field ExecuteBuffer

Specifies a <a href="https://msdn.microsoft.com/200f4e08-b5d3-484e-b87a-b3069dc3c99f">SURFACEALIGNMENT</a> structure that contains heap alignment requirements for surfaces tagged with DDSCAPS_EXECUTEBUFFER. 


### -field Overlay

Specifies a SURFACEALIGNMENT structure that contains heap alignment requirements for surfaces tagged with DDSCAPS_OVERLAY. 


### -field Texture

Specifies a SURFACEALIGNMENT structure that contains heap alignment requirements for surfaces tagged with DDSCAPS_TEXTURE. 


### -field ZBuffer

Specifies a <a href="https://msdn.microsoft.com/200f4e08-b5d3-484e-b87a-b3069dc3c99f">SURFACEALIGNMENT</a> structure that contains heap alignment requirements for surfaces tagged with DDSCAPS_ZBUFFER. 


### -field AlphaBuffer

Specifies a SURFACEALIGNMENT structure that contains heap alignment requirements for surfaces tagged with DDSCAPS_ALPHA. 


### -field Offscreen

Specifies a SURFACEALIGNMENT structure that contains heap alignment requirements for surfaces tagged with DDSCAPS_OFFSCREENPLAIN. 


### -field FlipTarget

Specifies a SURFACEALIGNMENT structure that contains heap alignment requirements for surfaces tagged with DDSCAPS_FLIP. 


## -remarks



The driver should verify that the <b>dwSize</b> member is at least as large as <b>sizeof</b>(HEAPALIGNMENT).




## -see-also




<a href="https://msdn.microsoft.com/e1ed1fa2-2f3c-4d04-a601-c11fb77eb5cc">DDSCAPS</a>



<a href="https://msdn.microsoft.com/200f4e08-b5d3-484e-b87a-b3069dc3c99f">SURFACEALIGNMENT</a>
 

 

