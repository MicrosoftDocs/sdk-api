---
UID: NF:dwrite_2.IDWriteFactory2.CreateGlyphRunAnalysis
title: IDWriteFactory2::CreateGlyphRunAnalysis
author: windows-sdk-content
description: Creates a glyph run analysis object, which encapsulates information used to render a glyph run.
old-location: directwrite\idwritefactory2_createglyphrunanalysis.htm
tech.root: DirectWrite
ms.assetid: 13cecfbf-8bb6-88a2-c8b2-3243f6cb92fd
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CreateGlyphRunAnalysis, CreateGlyphRunAnalysis method [Direct Write], CreateGlyphRunAnalysis method [Direct Write],IDWriteFactory2 interface, IDWriteFactory2 interface [Direct Write],CreateGlyphRunAnalysis method, IDWriteFactory2.CreateGlyphRunAnalysis, IDWriteFactory2::CreateGlyphRunAnalysis, directwrite.idwritefactory2_createglyphrunanalysis, dwrite_2/IDWriteFactory2::CreateGlyphRunAnalysis
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
 - IDWriteFactory2.CreateGlyphRunAnalysis
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dwrite_2.h
: 
- IDWriteFactory2.CreateGlyphRunAnalysis
: 
---

# IDWriteFactory2::CreateGlyphRunAnalysis


## -description


Creates a glyph run analysis object, which encapsulates information used to render a glyph run.


## -parameters




### -param glyphRun [in]

Type: <b>const <a href="https://msdn.microsoft.com/2997d63f-8d33-44c3-9617-cfffe5f61f7d">DWRITE_GLYPH_RUN</a>*</b>

Structure specifying the properties of the glyph run.


### -param transform [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/fe4bd8ba-fc3b-4a04-8a72-9983d52f4404">DWRITE_MATRIX</a>*</b>

Optional transform applied to the glyphs and their positions. This transform is applied after the
          scaling specified by the emSize and pixelsPerDip.


### -param renderingMode

Type: <b>DWRITE_RENDERING_MODE</b>

Specifies the rendering mode, which must be one of the raster rendering modes (i.e., not default
          and not outline).


### -param measuringMode

Type: <b><a href="https://msdn.microsoft.com/99e89754-8bc2-457d-bfdb-a3c9ccfe00c1">DWRITE_MEASURING_MODE</a></b>

Specifies the method to measure glyphs.


### -param gridFitMode

Type: <b><a href="https://msdn.microsoft.com/C32A6017-3711-482B-B806-79651163DEF6">DWRITE_GRID_FIT_MODE</a></b>

How to grid-fit glyph outlines. This must be non-default.


### -param antialiasMode

Type: <b><a href="https://msdn.microsoft.com/212B02C9-1265-4870-A059-F292640ECE15">DWRITE_TEXT_ANTIALIAS_MODE</a></b>

Specifies the antialias mode.


### -param baselineOriginX

Type: <b>FLOAT</b>

Horizontal position of the baseline origin, in DIPs.


### -param baselineOriginY

Type: <b>FLOAT</b>

Vertical position of the baseline origin, in DIPs.


### -param glyphRunAnalysis [out]

Type: <b><a href="https://msdn.microsoft.com/d4739b55-1a9b-4346-9b47-d8adb98df163">IDWriteGlyphRunAnalysis</a>**</b>

Receives a pointer to the newly created object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1D3EEC28-EAB3-4FA2-98E9-7A8FDAF6E6FE">IDWriteFactory2</a>
 

 

