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

# wglRealizeLayerPalette function


## -description


The <b>wglRealizeLayerPalette</b> function maps palette entries from a given color-index layer plane into the physical palette or initializes the palette of an RGBA layer plane.


## -parameters




### -param

TBD




#### - bRealize

Indicates whether the palette is to be realized into the physical palette. When <i>bRealize</i> is <b>TRUE</b>, the palette entries are mapped into the physical palette where available. When <i>bRealize</i> is <b>FALSE</b>, the palette entries for the layer plane of the window are no longer needed and might be released for use by another foreground window.


#### - hdc

Specifies the device context of a window whose layer plane palette is to be realized into the physical palette.


#### - iLayerPlane

Specifies the overlay or underlay plane. Positive values of <i>iLayerPlane</i> identify overlay planes, where 1 is the first overlay plane over the main plane, 2 is the second overlay plane over the first overlay plane, and so on. Negative values identify underlay planes, where 1 is the first underlay plane under the main plane, 2 is the second underlay plane under the first underlay plane, and so on. The number of overlay and underlay planes is given in the <b>bReserved</b> member of the <a href="https://msdn.microsoft.com/1480dea3-ae74-4e8b-b4de-fca8de5d8395">PIXELFORMATDESCRIPTOR</a> structure.


## -returns



If the function succeeds, the return value is <b>TRUE</b>, even if <i>bRealize</i> is <b>TRUE</b> and the physical palette is not available. If the function fails or when no pixel format is selected, the return value is <b>FALSE</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The physical palette for a layer plane is a shared resource among windows with layer planes. When more than one window attempts to realize a palette for a given physical layer plane, only one palette at a time is realized. When you call the <b>wglRealizeLayerPalette</b> function, the layer palette of a foreground window is always realized first.

When a window's layer palette is realized, its palette entries are always mapped one-to-one into the physical palette. Unlike GDI logical palettes, with <b>wglRealizeLayerPalette</b> there is no mapping of other windows' layer palettes to the current physical palette.

Whenever a window becomes the foreground window, call <b>wglRealizeLayerPalette</b> to realize its layer palettes again, even if the pixel type of the layer plane is RGBA.

Because <b>wglRealizeLayerPalette</b> doesn't realize the palette of the main plane, use GDI palette functions to realize the main plane palette.




## -see-also




<a href="https://msdn.microsoft.com/fdb0322d-503f-4c17-b438-f764d60da7f6">LAYERPLANEDESCRIPTOR</a>



<a href="https://msdn.microsoft.com/589a86f1-598d-4175-97fc-27ca0b254935">OpenGL on Windows</a>



<a href="https://msdn.microsoft.com/1480dea3-ae74-4e8b-b4de-fca8de5d8395">PIXELFORMATDESCRIPTOR</a>



<a href="https://msdn.microsoft.com/52053370-d88b-4faf-bdcd-4663c6d5270d">WGL Functions</a>



<a href="https://msdn.microsoft.com/a80d257e-7053-4328-8298-80ed72513837">wglDescribeLayerPlane</a>



<a href="https://msdn.microsoft.com/9f2d6f59-f1c6-44a5-8741-1ea4d84f5b2c">wglGetLayerPaletteEntries</a>



<a href="https://msdn.microsoft.com/083a563e-5b26-4ca8-8cae-c5a9ff901e8f">wglRealizeLayerPalette</a>



<a href="https://msdn.microsoft.com/bc44353d-15db-4e52-970d-a290b66bc046">wglSetLayerPaletteEntries</a>
 

 

