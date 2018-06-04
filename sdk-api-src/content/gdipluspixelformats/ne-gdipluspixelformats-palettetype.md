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

# PaletteType enumeration


## -description


The  <b>PaletteType</b> enumeration is used by the <a href="https://msdn.microsoft.com/8a692b2b-e9b1-465e-9bfa-7306cd1d7ced">Bitmap::InitializePalette</a> and <a href="https://msdn.microsoft.com/68641749-a274-41d7-b4ce-82999f9aac63">Bitmap::ConvertFormat</a> methods of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">Bitmap</a> class. The members of the enumeration identify several standard color palette formats.


## -enum-fields




### -field PaletteTypeCustom

An arbitrary custom palette provided by the caller.


### -field PaletteTypeOptimal

An palette of colors that are optimal for a particular bitmap. To create an optimal palette, pass PaletteTypeOptimal, the number of colors you want in the palette, and the address of a <a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">Bitmap</a> object to the <a href="https://msdn.microsoft.com/8a692b2b-e9b1-465e-9bfa-7306cd1d7ced">Bitmap::InitializePalette</a> method.


### -field PaletteTypeFixedBW

A palette that has two colors. This palette type is suitable for bitmaps that store 1 bit per pixel.


### -field PaletteTypeFixedHalftone8

A palette based on two intensities each (off or full) for the red, green, and blue channels. Also contains the 16 colors of the system palette. Because all eight of the on/off combinations of red, green, and blue are already in the system palette, this palette is the same as the system palette. This palette type is suitable for bitmaps that store 4 bits per pixel.


### -field PaletteTypeFixedHalftone27

A palette based on three intensities each for the red, green, and blue channels. Also contains the 16 colors of the system palette. Eight of the 16 system palette colors are among the 27 three-intensity combinations of red, green, and blue, so the total number of colors in the palette is 35. If the palette also includes the transparent color, the total number of colors is 36.


### -field PaletteTypeFixedHalftone64

A palette based on four intensities each for the red, green, and blue channels. Also contains the 16 colors of the system palette. Eight of the 16 system palette colors are among the 64 four-intensity combinations of red, green, and blue, so the total number of colors in the palette is 72. If the palette also includes the transparent color, the total number of colors is 73.


### -field PaletteTypeFixedHalftone125

A palette based on five intensities each for the red, green, and blue channels. Also contains the 16 colors of the system palette. Eight of the 16 system palette colors are among the 125 five-intensity combinations of red, green, and blue, so the total number of colors in the palette is 133. If the palette also includes the transparent color, the total number of colors is 134.


### -field PaletteTypeFixedHalftone216

A palette based on six intensities each for the red, green, and blue channels. Also contains the 16 colors of the system palette. Eight of the 16 system palette colors are among the 216 six-intensity combinations of red, green, and blue, so the total number of colors in the palette is 224. If the palette also includes the transparent color, the total number of colors is 225. This palette is sometimes called the Windows halftone palette or the Web palette.


### -field PaletteTypeFixedHalftone252

A palette based on 6 intensities of red, 7 intensities of green, and 6 intensities of blue. The system palette is not included. The total number of colors is 252. If the palette also includes the transparent color, the total number of colors is 253.


### -field PaletteTypeFixedHalftone256

A palette based on 8 intensities of red, 8 intensities of green, and 4 intensities of blue. The system palette is not included. The total number of colors is 256. If the transparent color is included in this palette, it must replace one of the RGB combinations.

