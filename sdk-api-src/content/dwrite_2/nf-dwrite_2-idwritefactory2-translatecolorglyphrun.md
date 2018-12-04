---
UID: NF:dwrite_2.IDWriteFactory2.TranslateColorGlyphRun
title: IDWriteFactory2::TranslateColorGlyphRun
author: windows-sdk-content
description: This method is called on a glyph run to translate it in to multiple color glyph runs.
old-location: directwrite\idwritefactory2_translatecolorglyphrun.htm
tech.root: DirectWrite
ms.assetid: 1D31F807-C3F2-466F-9723-E6F12B13BFA1
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: IDWriteFactory2 interface [Direct Write],TranslateColorGlyphRun method, IDWriteFactory2.TranslateColorGlyphRun, IDWriteFactory2::TranslateColorGlyphRun, TranslateColorGlyphRun, TranslateColorGlyphRun method [Direct Write], TranslateColorGlyphRun method [Direct Write],IDWriteFactory2 interface, directwrite.idwritefactory2_translatecolorglyphrun, dwrite_2/IDWriteFactory2::TranslateColorGlyphRun
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dwrite_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
req.dll: Dwrite.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteFactory2.TranslateColorGlyphRun
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFactory2::TranslateColorGlyphRun


## -description


This method is called on a glyph run to translate it in to multiple color glyph runs.


## -parameters




### -param baselineOriginX

Type: <b>FLOAT</b>

The horizontal baseline origin of the original glyph run.


### -param baselineOriginY

Type: <b>FLOAT</b>

The vertical baseline origin of the original glyph run.


### -param glyphRun [in]

Type: <b>const <a href="https://msdn.microsoft.com/2997d63f-8d33-44c3-9617-cfffe5f61f7d">DWRITE_GLYPH_RUN</a>*</b>

Original glyph run containing monochrome glyph IDs.


### -param glyphRunDescription [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/0fb25253-274a-42b7-8491-525d0550ce39">DWRITE_GLYPH_RUN_DESCRIPTION</a>*</b>

Optional glyph run description.


### -param measuringMode

Type: <b><a href="https://msdn.microsoft.com/99e89754-8bc2-457d-bfdb-a3c9ccfe00c1">DWRITE_MEASURING_MODE</a></b>

Measuring mode used to compute glyph positions if the run contains color glyphs.


### -param worldToDeviceTransform [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/fe4bd8ba-fc3b-4a04-8a72-9983d52f4404">DWRITE_MATRIX</a>*</b>

World transform multiplied by any DPI scaling. This is needed to compute glyph positions if the run contains color glyphs and the 
            measuring mode is not <a href="https://msdn.microsoft.com/99e89754-8bc2-457d-bfdb-a3c9ccfe00c1">DWRITE_MEASURING_MODE_NATURAL</a>. 
            If this parameter is <b>NULL</b>, and identity transform is assumed.
          


### -param colorPaletteIndex

Type: <b>UINT32</b>

Zero-based index of the color palette to use. Valid indices are less than the number of palettes in the font, as 
            returned by <a href="https://msdn.microsoft.com/99BB9C72-99B1-427C-B740-55A138189459">IDWriteFontFace2::GetColorPaletteCount</a>.
          


### -param colorLayers [out]

Type: <b><a href="https://msdn.microsoft.com/649AD648-32BB-4BF4-A82F-075E93505E33">IDWriteColorGlyphRunEnumerator</a>**</b>

If the original glyph run contains color glyphs, this parameter receives a pointer to 
            an <a href="https://msdn.microsoft.com/649AD648-32BB-4BF4-A82F-075E93505E33">IDWriteColorGlyphRunEnumerator</a> interface. 
            The client uses the returned interface to get information about glyph runs and associated colors to render instead of the original glyph run. 
            If the original glyph run does not contain color glyphs, this method returns <b>DWRITE_E_NOCOLOR</b> and the output pointer is <b>NULL</b>.
          


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the code calls this method with a glyph run that contains no color information, the method returns <b>DWRITE_E_NOCOLOR</b> to 
          let the application know that it can just draw the original glyph run. If the glyph run contains color information, the function returns an object
          that can be enumerated through to expose runs and associated colors. The application then 
          calls <a href="https://msdn.microsoft.com/95a0044c-dffd-4c6a-a6eb-2f87b02ef89a">DrawGlyphRun</a> with each of the returned glyph runs and foreground colors.
        




## -see-also




<a href="https://msdn.microsoft.com/1D3EEC28-EAB3-4FA2-98E9-7A8FDAF6E6FE">IDWriteFactory2</a>
 

 

