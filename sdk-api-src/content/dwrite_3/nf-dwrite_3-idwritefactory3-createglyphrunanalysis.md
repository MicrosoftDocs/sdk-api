---
UID: NF:dwrite_3.IDWriteFactory3.CreateGlyphRunAnalysis
title: IDWriteFactory3::CreateGlyphRunAnalysis
author: windows-sdk-content
description: Creates a glyph-run-analysis object that encapsulates info that DirectWrite uses to render a glyph run.
old-location: directwrite\idwritefactory3_createglyphrunanalysis.htm
tech.root: DirectWrite
ms.assetid: 5BF8BA9C-F07F-43F0-B712-71220E6535A5
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: CreateGlyphRunAnalysis, CreateGlyphRunAnalysis method [Direct Write], CreateGlyphRunAnalysis method [Direct Write],IDWriteFactory3 interface, IDWriteFactory3 interface [Direct Write],CreateGlyphRunAnalysis method, IDWriteFactory3.CreateGlyphRunAnalysis, IDWriteFactory3::CreateGlyphRunAnalysis, directwrite.idwritefactory3_createglyphrunanalysis, dwrite_3/IDWriteFactory3::CreateGlyphRunAnalysis
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - IDWriteFactory3.CreateGlyphRunAnalysis
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFactory3::CreateGlyphRunAnalysis


## -description


Creates a glyph-run-analysis object that encapsulates info that <a href="https://msdn.microsoft.com/62a8d723-ae1c-4cbc-a9da-3177e80d4a3a">DirectWrite</a> uses to render a glyph run.
        


## -parameters




### -param glyphRun [in]

Type: <b><a href="https://msdn.microsoft.com/2997d63f-8d33-44c3-9617-cfffe5f61f7d">DWRITE_GLYPH_RUN</a></b>

A <a href="https://msdn.microsoft.com/2997d63f-8d33-44c3-9617-cfffe5f61f7d">DWRITE_GLYPH_RUN</a> structure that contains the properties of the glyph run.
          


### -param transform [in, optional]

Type: <b><a href="https://msdn.microsoft.com/fe4bd8ba-fc3b-4a04-8a72-9983d52f4404">DWRITE_MATRIX</a></b>

A <a href="https://msdn.microsoft.com/fe4bd8ba-fc3b-4a04-8a72-9983d52f4404">DWRITE_MATRIX</a> structure that describes the optional transform to be applied to glyphs and their positions. 


### -param renderingMode

Type: <b><a href="https://msdn.microsoft.com/CAA88479-FE39-48D0-89D8-CEA0C922428A">DWRITE_RENDERING_MODE1</a></b>

A <a href="https://msdn.microsoft.com/CAA88479-FE39-48D0-89D8-CEA0C922428A">DWRITE_RENDERING_MODE1</a>-typed value that specifies the rendering mode, which must be one of the raster rendering modes (that is, not default and not outline).
          


### -param measuringMode

Type: <b><a href="https://msdn.microsoft.com/99e89754-8bc2-457d-bfdb-a3c9ccfe00c1">DWRITE_MEASURING_MODE</a></b>

A <a href="https://msdn.microsoft.com/99e89754-8bc2-457d-bfdb-a3c9ccfe00c1">DWRITE_MEASURING_MODE</a>-typed value that specifies the measuring method for glyphs in the run. This method uses this value with the other properties to determine the rendering mode.
          


### -param gridFitMode

Type: <b><a href="https://msdn.microsoft.com/C32A6017-3711-482B-B806-79651163DEF6">DWRITE_GRID_FIT_MODE</a></b>

A <a href="https://msdn.microsoft.com/C32A6017-3711-482B-B806-79651163DEF6">DWRITE_GRID_FIT_MODE</a>-typed value that specifies how to grid-fit glyph outlines. This value must be non-default.
          


### -param antialiasMode

Type: <b><a href="https://msdn.microsoft.com/212B02C9-1265-4870-A059-F292640ECE15">DWRITE_TEXT_ANTIALIAS_MODE</a></b>

A <a href="https://msdn.microsoft.com/212B02C9-1265-4870-A059-F292640ECE15">DWRITE_TEXT_ANTIALIAS_MODE</a>-typed value that specifies the type of antialiasing to use for text when the rendering mode calls for antialiasing.
          


### -param baselineOriginX

Type: <b>FLOAT</b>

The horizontal position of the baseline origin, in DIPs, relative to the upper-left corner of the DIB.
          


### -param baselineOriginY

Type: <b>FLOAT</b>

The vertical position of the baseline origin, in DIPs, relative to the upper-left corner of the DIB.
          


### -param glyphRunAnalysis [out]

Type: <b><a href="https://msdn.microsoft.com/d4739b55-1a9b-4346-9b47-d8adb98df163">IDWriteGlyphRunAnalysis</a>**</b>

A pointer to a memory block that receives a pointer to a <a href="https://msdn.microsoft.com/d4739b55-1a9b-4346-9b47-d8adb98df163">IDWriteGlyphRunAnalysis</a> interface for the newly created glyph-run-analysis object.
          


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/CCE68F89-6945-40F4-9C27-285AC8AB4D0B">IDWriteFactory3</a>
 

 

