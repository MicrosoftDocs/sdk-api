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

# DitherType enumeration


## -description


The <b>DitherType</b> enumeration identifies the available algorithms for dithering when a bitmap is converted. 

Calling the <a href="https://msdn.microsoft.com/68641749-a274-41d7-b4ce-82999f9aac63">Bitmap::ConvertFormat</a> method of a <a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">Bitmap</a> object changes the pixel format of that <b>Bitmap</b>. If the conversion results in a reduced bit depth (fewer bits per pixel), then certain colors in the original bitmap will be simulated by a dither (checkerboard) pattern made up of colors that are available in the new pixel format. The members of the <b>DitherType</b> enumeration identify the algorithms available for performing this dithering.


## -enum-fields




### -field DitherTypeNone

No dithering is performed. Pixels in the source bitmap are mapped to the nearest color in the palette specified by the <i>palette</i> parameter of the <a href="https://msdn.microsoft.com/68641749-a274-41d7-b4ce-82999f9aac63">Bitmap::ConvertFormat</a> method. This algorithm can be used with any palette. If the palette specified by the <i>palette</i> parameter does not have one of the standard fixed formats listed in the <a href="https://msdn.microsoft.com/8ab8678e-3a48-4747-8f1e-4c7fad370001">PaletteType</a> enumeration, pass <b>PaletteTypeCustom</b> to the <i>palettetype</i> parameter.


### -field DitherTypeSolid

No dithering is performed. Pixels in the source bitmap are mapped to the nearest color in the palette specified by the <i>palette</i> parameter of the <a href="https://msdn.microsoft.com/68641749-a274-41d7-b4ce-82999f9aac63">Bitmap::ConvertFormat</a> method. This algorithm can be used with any palette. If the palette specified by the <i>palette</i> parameter does not have one of the standard fixed formats listed in the <a href="https://msdn.microsoft.com/8ab8678e-3a48-4747-8f1e-4c7fad370001">PaletteType</a> enumeration, pass <b>PaletteTypeCustom</b> to the <i>palettetype</i> parameter.


### -field DitherTypeOrdered4x4

You can use this algorithm to perform dithering based on the colors in one of the standard fixed palettes. You can also use this algorithm to convert a bitmap to a 16-bits-per-pixel format that has no palette.


### -field DitherTypeOrdered8x8

Dithering is performed using the colors in one of the standard fixed palettes.


### -field DitherTypeOrdered16x16

Dithering is performed using the colors in one of the standard fixed palettes.


### -field DitherTypeSpiral4x4

Dithering is performed using the colors in one of the standard fixed palettes.


### -field DitherTypeSpiral8x8

Dithering is performed using the colors in one of the standard fixed palettes.


### -field DitherTypeDualSpiral4x4

Dithering is performed using the colors in one of the standard fixed palettes.


### -field DitherTypeDualSpiral8x8

Dithering is performed using the colors in one of the standard fixed palettes.


### -field DitherTypeErrorDiffusion

Dithering is performed based on the palette specified by the <i>palette</i> parameter of the <a href="https://msdn.microsoft.com/68641749-a274-41d7-b4ce-82999f9aac63">Bitmap::ConvertFormat</a> method. This algorithm can be used with any palette. If the palette specified by the <i>palette</i> parameter does not have one of the standard fixed formats listed in the <a href="https://msdn.microsoft.com/8ab8678e-3a48-4747-8f1e-4c7fad370001">PaletteType</a> enumeration, pass <b>PaletteTypeCustom</b> to the <i>palettetype</i> parameter.


### -field DitherTypeMax




#### - DitherTypeOrdered91x91

Dithering is performed using the colors in one of the standard fixed palettes.


## -remarks



If you pass any of the ordered or spiral dither types (except <b>DitherTypeOrdered4x4</b>) to the <i>dithertype</i> parameter of the <a href="https://msdn.microsoft.com/68641749-a274-41d7-b4ce-82999f9aac63">Bitmap::ConvertFormat</a> method, you must pass one of the following fixed palette types to the <i>palettetype</i> parameter.

<ul>
<li><b>PaletteTypeFixedBW</b></li>
<li><b>PaletteTypeFixedHalftone8</b></li>
<li><b>PaletteTypeFixedHalftone27</b></li>
<li><b>PaletteTypeFixedHalftone64</b></li>
<li><b>PaletteTypeFixedHalftone125</b></li>
<li><b>PaletteTypeFixedHalftone216</b></li>
<li><b>PaletteTypeFixedHalftone252</b></li>
<li><b>PaletteTypeFixedHalftone256</b></li>
</ul>
The <b>DitherTypeOrdered4x4</b> algorithm is a special case. You can use it with the fixed palette types shown in the preceding list or you can use it to convert a bitmap to a 16-bits-per-pixel format.



