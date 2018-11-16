---
UID: NF:dwrite_3.IDWriteFactory4.TranslateColorGlyphRun
title: IDWriteFactory4::TranslateColorGlyphRun
author: windows-sdk-content
description: Translates a glyph run to a sequence of color glyph runs, which can be rendered to produce a color representation of the original &#0034;base&#0034; run.
old-location: directwrite\idwritefactory4_translatecolorglyphrun.htm
tech.root: DirectWrite
ms.assetid: D8C38635-8D7B-4C05-87D5-CCDCF31A4070
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IDWriteFactory4 interface [Direct Write],TranslateColorGlyphRun method, IDWriteFactory4.TranslateColorGlyphRun, IDWriteFactory4::TranslateColorGlyphRun, TranslateColorGlyphRun, TranslateColorGlyphRun method [Direct Write], TranslateColorGlyphRun method [Direct Write],IDWriteFactory4 interface, directwrite.idwritefactory4_translatecolorglyphrun, dwrite_3/IDWriteFactory4::TranslateColorGlyphRun
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dwrite_3.h
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
req.lib: Dwrite.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dwrite.lib
 - Dwrite.dll
api_name:
 - IDWriteFactory4.TranslateColorGlyphRun
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dwrite_3.h
: 
- IDWriteFactory4.TranslateColorGlyphRun
: 
---

# IDWriteFactory4::TranslateColorGlyphRun


## -description


Translates a glyph run to a sequence of color glyph runs, which can be rendered to produce a color representation of the original "base" run.


## -parameters




### -param baselineOrigin

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

Horizontal and vertical origin of the base glyph run in pre-transform coordinates.


### -param glyphRun [in]

Type: <b><a href="https://msdn.microsoft.com/2997d63f-8d33-44c3-9617-cfffe5f61f7d">DWRITE_GLYPH_RUN</a></b>

Pointer to the original "base" glyph run.


### -param glyphRunDescription [in, optional]

Type: <b><a href="https://msdn.microsoft.com/0fb25253-274a-42b7-8491-525d0550ce39">DWRITE_GLYPH_RUN_DESCRIPTION</a></b>

Optional glyph run description.


### -param desiredGlyphImageFormats

Type: <b><a href="https://msdn.microsoft.com/ECC868B5-3D17-4D55-8E00-AB446C1C22FE">DWRITE_GLYPH_IMAGE_FORMATS</a></b>

Which data formats the runs should be split into.


### -param measuringMode

Type: <b><a href="https://msdn.microsoft.com/99e89754-8bc2-457d-bfdb-a3c9ccfe00c1">DWRITE_MEASURING_MODE</a></b>

Measuring mode, needed to compute the origins of each glyph.


### -param worldAndDpiTransform [in, optional]

Type: <b><a href="https://msdn.microsoft.com/fe4bd8ba-fc3b-4a04-8a72-9983d52f4404">DWRITE_MATRIX</a></b>

Matrix converting from the client's coordinate space to device coordinates (pixels), i.e., the world transform multiplied by any DPI scaling.


### -param colorPaletteIndex

Type: <b>UINT32</b>

Zero-based index of the color palette to use.
          Valid indices are less than the number of palettes in the font, as returned
          by <a href="https://msdn.microsoft.com/99BB9C72-99B1-427C-B740-55A138189459">IDWriteFontFace2::GetColorPaletteCount</a>.


### -param colorLayers [out]

Type: <b><a href="https://msdn.microsoft.com/692CB5FF-3E74-4D3E-B961-E4AF5995A1B2">IDWriteColorGlyphRunEnumerator1</a>**</b>

If the function succeeds, receives a pointer to an enumerator object that can be used to obtain the color glyph runs.
          If the base run has no color glyphs, then the output pointer is NULL and the method returns DWRITE_E_NOCOLOR.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns DWRITE_E_NOCOLOR if the font has no color information, the glyph run
          does not contain any color glyphs, or the specified color palette index
          is out of range. In this case, the client should render the original glyph 
          run. Otherwise, returns a standard HRESULT error code.




## -remarks



Calling <a href="https://msdn.microsoft.com/1D31F807-C3F2-466F-9723-E6F12B13BFA1">IDWriteFactory2::TranslateColorGlyphRun</a> is equivalent 
        to calling <b>IDWriteFactory4::TranslateColorGlyph</b> run with the following formats specified: DWRITE_GLYPH_IMAGE_FORMATS_TRUETYPE|DWRITE_GLYPH_IMAGE_FORMATS_CFF|DWRITE_GLYPH_IMAGE_FORMATS_COLR.




## -see-also




<a href="https://msdn.microsoft.com/D3C5E48A-A062-430A-A196-CAC621F346FC">IDWriteFactory4</a>
 

 

