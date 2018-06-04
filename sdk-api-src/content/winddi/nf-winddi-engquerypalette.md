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

# EngQueryPalette function


## -description


The <b>EngQueryPalette</b> function queries the specified palette for its attributes.


## -parameters




### -param hpal

TBD


### -param piMode

Pointer to a location that receives the palette mode, as originally specified in <a href="https://msdn.microsoft.com/library/windows/hardware/ff564212">EngCreatePalette</a>.


### -param cColors

Specifies the number of entries in the buffer to which <i>pulColors</i> points. The return value depends on whether <i>cColors</i> is negative.


### -param pulColors

Pointer to a buffer that receives the palette color information. If <i>cColors</i> is zero, <i>pulColors</i> can be <b>NULL</b>.


#### - hPal

Handle to the palette to be queried.


## -returns



When <i>cColors</i> is zero, <b>EngQueryPalette</b> returns the number of palette entries required in the buffer to which <i>pulColors</i> points in order to return the palette color information. When <i>cColors</i> is nonzero and <i>pulColors</i> is not <b>NULL</b>, <b>EngQueryPalette</b> returns the number of entries written in the buffer to which <i>pulColors</i> points. 




## -remarks



If the palette mode is PAL_BITFIELDS, PAL_RGB, or PAL_BGR and the buffer that <i>pulColors</i> points to is large enough, <i>pulColors</i> points to three ULONG masks that represent the red, green, and blue color masks of the palette.

If the palette mode is PAL_INDEXED and the buffer that <i>pulColors</i> points to is large enough, <i>pulColors</i> contains all of the 24-bit RGB values that represent the palette colors.

A driver must test for the presence of the GCAPS_PALMANAGED flag to determine whether the colors represent a fixed or a changeable palette.

<b>EngQueryPalette</b> is intended for use by mirroring drivers that need to know the color format of the primary display. A mirroring driver typically calls this function in its <a href="https://msdn.microsoft.com/library/windows/hardware/ff556211">DrvEnablePDEV</a> routine.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556211">DrvEnablePDEV</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564212">EngCreatePalette</a>
 

 

