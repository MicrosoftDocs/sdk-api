---
UID: NE:gdipluspixelformats.DitherType
title: DitherType
author: windows-sdk-content
description: The DitherType enumeration identifies the available algorithms for dithering when a bitmap is converted.
old-location: gdiplus\_gdiplus_ENUM_DitherType.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\dithertype.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: DitherType, DitherType enumeration [GDI+], DitherTypeDualSpiral4x4, DitherTypeDualSpiral8x8, DitherTypeErrorDiffusion, DitherTypeNone, DitherTypeOrdered16x16, DitherTypeOrdered4x4, DitherTypeOrdered8x8, DitherTypeOrdered91x91, DitherTypeSolid, DitherTypeSpiral4x4, DitherTypeSpiral8x8, _gdiplus_ENUM_DitherType, gdiplus._gdiplus_ENUM_DitherType, gdipluspixelformats/DitherType, gdipluspixelformats/DitherTypeDualSpiral4x4, gdipluspixelformats/DitherTypeDualSpiral8x8, gdipluspixelformats/DitherTypeErrorDiffusion, gdipluspixelformats/DitherTypeNone, gdipluspixelformats/DitherTypeOrdered16x16, gdipluspixelformats/DitherTypeOrdered4x4, gdipluspixelformats/DitherTypeOrdered8x8, gdipluspixelformats/DitherTypeOrdered91x91, gdipluspixelformats/DitherTypeSolid, gdipluspixelformats/DitherTypeSpiral4x4, gdipluspixelformats/DitherTypeSpiral8x8
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: gdipluspixelformats.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - gdipluspixelformats.h
api_name:
 - DitherType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.1
---

# DitherType enumeration


## -description


The <b>DitherType</b> enumeration identifies the available algorithms for dithering when a bitmap is converted. 

Calling the <a href="https://msdn.microsoft.com/en-us/library/ms536306(v=VS.85).aspx">Bitmap::ConvertFormat</a> method of a <a href="https://msdn.microsoft.com/en-us/library/ms534420(v=VS.85).aspx">Bitmap</a> object changes the pixel format of that <b>Bitmap</b>. If the conversion results in a reduced bit depth (fewer bits per pixel), then certain colors in the original bitmap will be simulated by a dither (checkerboard) pattern made up of colors that are available in the new pixel format. The members of the <b>DitherType</b> enumeration identify the algorithms available for performing this dithering.


## -enum-fields




### -field DitherTypeNone

No dithering is performed. Pixels in the source bitmap are mapped to the nearest color in the palette specified by the <i>palette</i> parameter of the <a href="https://msdn.microsoft.com/en-us/library/ms536306(v=VS.85).aspx">Bitmap::ConvertFormat</a> method. This algorithm can be used with any palette. If the palette specified by the <i>palette</i> parameter does not have one of the standard fixed formats listed in the <a href="https://msdn.microsoft.com/en-us/library/ms534159(v=VS.85).aspx">PaletteType</a> enumeration, pass <b>PaletteTypeCustom</b> to the <i>palettetype</i> parameter.


### -field DitherTypeSolid

No dithering is performed. Pixels in the source bitmap are mapped to the nearest color in the palette specified by the <i>palette</i> parameter of the <a href="https://msdn.microsoft.com/en-us/library/ms536306(v=VS.85).aspx">Bitmap::ConvertFormat</a> method. This algorithm can be used with any palette. If the palette specified by the <i>palette</i> parameter does not have one of the standard fixed formats listed in the <a href="https://msdn.microsoft.com/en-us/library/ms534159(v=VS.85).aspx">PaletteType</a> enumeration, pass <b>PaletteTypeCustom</b> to the <i>palettetype</i> parameter.


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

Dithering is performed based on the palette specified by the <i>palette</i> parameter of the <a href="https://msdn.microsoft.com/en-us/library/ms536306(v=VS.85).aspx">Bitmap::ConvertFormat</a> method. This algorithm can be used with any palette. If the palette specified by the <i>palette</i> parameter does not have one of the standard fixed formats listed in the <a href="https://msdn.microsoft.com/en-us/library/ms534159(v=VS.85).aspx">PaletteType</a> enumeration, pass <b>PaletteTypeCustom</b> to the <i>palettetype</i> parameter.


### -field DitherTypeMax




#### - DitherTypeOrdered91x91

Dithering is performed using the colors in one of the standard fixed palettes.


## -remarks



If you pass any of the ordered or spiral dither types (except <b>DitherTypeOrdered4x4</b>) to the <i>dithertype</i> parameter of the <a href="https://msdn.microsoft.com/en-us/library/ms536306(v=VS.85).aspx">Bitmap::ConvertFormat</a> method, you must pass one of the following fixed palette types to the <i>palettetype</i> parameter.

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



