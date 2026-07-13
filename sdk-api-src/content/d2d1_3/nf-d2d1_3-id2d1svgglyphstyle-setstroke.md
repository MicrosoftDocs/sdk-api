---
UID: NF:d2d1_3.ID2D1SvgGlyphStyle.SetStroke
title: ID2D1SvgGlyphStyle::SetStroke (d2d1_3.h)
description: Provides values to an SVG glyph for stroke properties. The brush with opacity set to 1 is used as the 'context-stroke'. The opacity of the brush is used as the 'context-stroke-opacity' value.
helpviewer_keywords: ["ID2D1SvgGlyphStyle interface [Direct2D]","SetStroke method","ID2D1SvgGlyphStyle.SetStroke","ID2D1SvgGlyphStyle::SetStroke","SetStroke","SetStroke method [Direct2D]","SetStroke method [Direct2D]","ID2D1SvgGlyphStyle interface","d2d1_3/ID2D1SvgGlyphStyle::SetStroke","direct2d.id2d1svgglyphstyle_setstroke"]
old-location: direct2d\id2d1svgglyphstyle_setstroke.htm
tech.root: Direct2D
ms.assetid: 3C7734DF-3EA6-43A8-8913-8D174ABAAA56
ms.date: 12/05/2018
ms.keywords: ID2D1SvgGlyphStyle interface [Direct2D],SetStroke method, ID2D1SvgGlyphStyle.SetStroke, ID2D1SvgGlyphStyle::SetStroke, SetStroke, SetStroke method [Direct2D], SetStroke method [Direct2D],ID2D1SvgGlyphStyle interface, d2d1_3/ID2D1SvgGlyphStyle::SetStroke, direct2d.id2d1svgglyphstyle_setstroke
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1SvgGlyphStyle::SetStroke
 - d2d1_3/ID2D1SvgGlyphStyle::SetStroke
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1SvgGlyphStyle.SetStroke
---

# ID2D1SvgGlyphStyle::SetStroke


## -description

Provides values to an SVG glyph for stroke properties. The brush with opacity
        set to 1 is used as the 'context-stroke'. The opacity of the brush is used as
        the 'context-stroke-opacity' value.

## -parameters

### -param brush [in, optional]

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>*</b>

Describes how the stroke is painted. A null brush will cause the context-stroke value to be none.

### -param strokeWidth

Type: <b>FLOAT</b>

Specifies the 'context-value' for the 'stroke-width' property.

### -param dashes [in, optional]

Type: <b>const FLOAT*</b>

Specifies the 'context-value' for the 'stroke-dasharray'
          property. A null value will cause the stroke-dasharray to be set to 'none'.

### -param dashesCount

Type: <b>UINT32</b>

The number of dashes in the dash array.

### -param dashOffset

Type: <b>FLOAT</b>

Specifies the 'context-value' for the 'stroke-dashoffset' property.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code.

## -see-also

<a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1svgglyphstyle">ID2D1SvgGlyphStyle</a>