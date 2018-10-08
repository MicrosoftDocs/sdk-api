---
UID: NF:d2d1_3.ID2D1DeviceContext4.DrawColorBitmapGlyphRun
title: ID2D1DeviceContext4::DrawColorBitmapGlyphRun
author: windows-sdk-content
description: Draws a color bitmap glyph run using one of the bitmap formats.
old-location: direct2d\id2d1devicecontext4_drawcolorbitmapglyphrun.htm
tech.root: Direct2D
ms.assetid: E3DDC924-87A1-43C7-8FC7-3C4E3FC2AC59
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: DrawColorBitmapGlyphRun, DrawColorBitmapGlyphRun method [Direct2D], DrawColorBitmapGlyphRun method [Direct2D],ID2D1DeviceContext4 interface, ID2D1DeviceContext4 interface [Direct2D],DrawColorBitmapGlyphRun method, ID2D1DeviceContext4.DrawColorBitmapGlyphRun, ID2D1DeviceContext4::DrawColorBitmapGlyphRun, d2d1_3/ID2D1DeviceContext4::DrawColorBitmapGlyphRun, direct2d.id2d1devicecontext4_drawcolorbitmapglyphrun
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1_3.h
req.include-header: 
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
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1DeviceContext4.DrawColorBitmapGlyphRun
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DeviceContext4::DrawColorBitmapGlyphRun


## -description


Draws a color bitmap glyph run using one of the bitmap formats.


## -parameters




### -param glyphImageFormat

Type: <b><a href="https://msdn.microsoft.com/ECC868B5-3D17-4D55-8E00-AB446C1C22FE">DWRITE_GLYPH_IMAGE_FORMATS</a></b>

Specifies the format of the glyph image. Supported formats are DWRITE_GLYPH_IMAGE_FORMATS_PNG, DWRITE_GLYPH_IMAGE_FORMATS_JPEG,
          DWRITE_GLYPH_IMAGE_FORMATS_TIFF, or DWRITE_GLYPH_IMAGE_FORMATS_PREMULTIPLIED_B8G8R8A8.  This method will result in an error if the color glyph run does not contain the requested format.
          

Only one format can be specified at a time, combinations of flags are not valid input.


### -param baselineOrigin

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The origin of the baseline for the glyph run.


### -param glyphRun [in]

Type: <b>const <a href="https://msdn.microsoft.com/2997d63f-8d33-44c3-9617-cfffe5f61f7d">DWRITE_GLYPH_RUN</a>*</b>

The glyphs to render.


### -param measuringMode

Type: <b><a href="https://msdn.microsoft.com/99e89754-8bc2-457d-bfdb-a3c9ccfe00c1">DWRITE_MEASURING_MODE</a></b>

Indicates the measuring method.


### -param bitmapSnapOption

Type: <b><a href="https://msdn.microsoft.com/14D99AFE-8072-4EAC-8932-6BD8D6EACB48">D2D1_COLOR_BITMAP_GLYPH_SNAP_OPTION</a></b>

Specifies the pixel snapping policy when rendering color bitmap glyphs.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/59E1F73B-BAD9-4826-BF5B-435E760CC546">ID2D1DeviceContext4</a>
 

 

