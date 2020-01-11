---
UID: NF:dwrite_3.IDWriteFactory4.ComputeGlyphOrigins(DWRITE_GLYPH_RUN const,DWRITE_MEASURING_MODE,D2D1_POINT_2F,DWRITE_MATRIX const,D2D1_POINT_2F)
title: IDWriteFactory4::ComputeGlyphOrigins(DWRITE_GLYPH_RUN const,DWRITE_MEASURING_MODE,D2D1_POINT_2F,DWRITE_MATRIX const,D2D1_POINT_2F) (dwrite_3.h)
description: Converts glyph run placements to glyph origins.
old-location: directwrite\idwritefactory4_computeglyphorigins.htm
tech.root: DirectWrite
ms.assetid: 0AA609E2-28C3-4D0C-A627-0648FB0D126A
ms.date: 12/05/2018
ms.keywords: ComputeGlyphOrigins, ComputeGlyphOrigins method [Direct Write], ComputeGlyphOrigins method [Direct Write],IDWriteFactory4 interface, IDWriteFactory4 interface [Direct Write],ComputeGlyphOrigins method, IDWriteFactory4.ComputeGlyphOrigins, IDWriteFactory4.ComputeGlyphOrigins(DWRITE_GLYPH_RUN const,DWRITE_MEASURING_MODE,D2D1_POINT_2F,DWRITE_MATRIX const,D2D1_POINT_2F), IDWriteFactory4::ComputeGlyphOrigins, IDWriteFactory4::ComputeGlyphOrigins(DWRITE_GLYPH_RUN const,DWRITE_MEASURING_MODE,D2D1_POINT_2F,DWRITE_MATRIX const,D2D1_POINT_2F), directwrite.idwritefactory4_computeglyphorigins, dwrite_3/IDWriteFactory4::ComputeGlyphOrigins
f1_keywords:
- dwrite_3/IDWriteFactory4.ComputeGlyphOrigins
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteFactory4::ComputeGlyphOrigins(DWRITE_GLYPH_RUN const,DWRITE_MEASURING_MODE,D2D1_POINT_2F,DWRITE_MATRIX const,D2D1_POINT_2F)


## -description


Converts glyph run placements to glyph origins.


## -parameters




### -param glyphRun

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run">DWRITE_GLYPH_RUN</a></b>

Structure containing the properties of the glyph run.


#### - measuringMode

Type: <b><a href="/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode">DWRITE_MEASURING_MODE</a></b>

The measuring method for glyphs in the run, used with the other properties to determine the rendering mode.


### -param baselineOrigin

Type: <b><a href="/windows/win32/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a></b>

The position of the baseline origin, in DIPs, relative to the upper-left corner of the DIB.


#### - worldAndDpiTransform [in, optional]

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix">DWRITE_MATRIX</a></b>

World transform multiplied by any DPI scaling. 
          This is needed to compute glyph positions if the run contains color glyphs and the measuring mode is not <a href="/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode">DWRITE_MEASURING_MODE_NATURAL</a>. 
          If this parameter is NULL, and identity transform is assumed. 


### -param glyphOrigins [out]

Type: <b><a href="/windows/win32/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a>*</b>

On return contains the glyph origins for the glyphrun.


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns S_OK. Otherwise, it returns an HRESULT error code.




## -remarks



The transform and DPI have no effect on the origin scaling. They are solely used to compute glyph advances when not supplied and align glyphs in pixel aligned measuring modes.




## -see-also




<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory4">IDWriteFactory4</a>
 

 

