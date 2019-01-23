---
UID: NF:dwrite_3.IDWriteFactory4.ComputeGlyphOrigins(DWRITE_GLYPH_RUN const,D2D1_POINT_2F,D2D1_POINT_2F)
title: IDWriteFactory4::ComputeGlyphOrigins(DWRITE_GLYPH_RUN const,D2D1_POINT_2F,D2D1_POINT_2F)
author: windows-sdk-content
description: Converts glyph run placements to glyph origins.
old-location: directwrite\idwritefactory4_computeglyphorigins.htm
tech.root: DirectWrite
ms.assetid: 0AA609E2-28C3-4D0C-A627-0648FB0D126A
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ComputeGlyphOrigins, ComputeGlyphOrigins method [Direct Write], ComputeGlyphOrigins method [Direct Write],IDWriteFactory4 interface, IDWriteFactory4 interface [Direct Write],ComputeGlyphOrigins method, IDWriteFactory4.ComputeGlyphOrigins, IDWriteFactory4.ComputeGlyphOrigins(DWRITE_GLYPH_RUN const,D2D1_POINT_2F,D2D1_POINT_2F), IDWriteFactory4::ComputeGlyphOrigins, IDWriteFactory4::ComputeGlyphOrigins(DWRITE_GLYPH_RUN const,D2D1_POINT_2F,D2D1_POINT_2F), directwrite.idwritefactory4_computeglyphorigins, dwrite_3/IDWriteFactory4::ComputeGlyphOrigins
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
 - IDWriteFactory4.ComputeGlyphOrigins
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFactory4::ComputeGlyphOrigins(DWRITE_GLYPH_RUN const,D2D1_POINT_2F,D2D1_POINT_2F)


## -description


Converts glyph run placements to glyph origins.


## -parameters




### -param glyphRun

Type: <b><a href="https://msdn.microsoft.com/2997d63f-8d33-44c3-9617-cfffe5f61f7d">DWRITE_GLYPH_RUN</a></b>

Structure containing the properties of the glyph run.


### -param baselineOrigin

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The position of the baseline origin, in DIPs, relative to the upper-left corner of the DIB.


### -param glyphOrigins [out]

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a>*</b>

On return contains the glyph origins for the glyphrun.


#### - measuringMode

Type: <b><a href="https://msdn.microsoft.com/99e89754-8bc2-457d-bfdb-a3c9ccfe00c1">DWRITE_MEASURING_MODE</a></b>

The measuring method for glyphs in the run, used with the other properties to determine the rendering mode.


#### - worldAndDpiTransform [in, optional]

Type: <b><a href="https://msdn.microsoft.com/fe4bd8ba-fc3b-4a04-8a72-9983d52f4404">DWRITE_MATRIX</a></b>

World transform multiplied by any DPI scaling. 
          This is needed to compute glyph positions if the run contains color glyphs and the measuring mode is not <a href="https://msdn.microsoft.com/99e89754-8bc2-457d-bfdb-a3c9ccfe00c1">DWRITE_MEASURING_MODE_NATURAL</a>. 
          If this parameter is NULL, and identity transform is assumed. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If this method succeeds, it returns S_OK. Otherwise, it returns an HRESULT error code.




## -remarks



The transform and DPI have no effect on the origin scaling. They are solely used to compute glyph advances when not supplied and align glyphs in pixel aligned measuring modes.




## -see-also




<a href="https://msdn.microsoft.com/D3C5E48A-A062-430A-A196-CAC621F346FC">IDWriteFactory4</a>
 

 

