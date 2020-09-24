---
UID: NF:d2d1_3.ID2D1SvgGlyphStyle.SetFill
title: ID2D1SvgGlyphStyle::SetFill (d2d1_3.h)
description: Provides values to an SVG glyph for fill.
helpviewer_keywords: ["ID2D1SvgGlyphStyle interface [Direct2D]","SetFill method","ID2D1SvgGlyphStyle.SetFill","ID2D1SvgGlyphStyle::SetFill","SetFill","SetFill method [Direct2D]","SetFill method [Direct2D]","ID2D1SvgGlyphStyle interface","d2d1_3/ID2D1SvgGlyphStyle::SetFill","direct2d.id2d1svgglyphstyle_setfill"]
old-location: direct2d\id2d1svgglyphstyle_setfill.htm
tech.root: Direct2D
ms.assetid: 7F8D423C-6A3A-4240-87E9-515F5FE29C1D
ms.date: 12/05/2018
ms.keywords: ID2D1SvgGlyphStyle interface [Direct2D],SetFill method, ID2D1SvgGlyphStyle.SetFill, ID2D1SvgGlyphStyle::SetFill, SetFill, SetFill method [Direct2D], SetFill method [Direct2D],ID2D1SvgGlyphStyle interface, d2d1_3/ID2D1SvgGlyphStyle::SetFill, direct2d.id2d1svgglyphstyle_setfill
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
 - ID2D1SvgGlyphStyle::SetFill
 - d2d1_3/ID2D1SvgGlyphStyle::SetFill
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
 - ID2D1SvgGlyphStyle.SetFill
---

# ID2D1SvgGlyphStyle::SetFill


## -description

Provides values to an SVG glyph for fill.

## -parameters

### -param brush [in, optional]

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>*</b>

Describes how the area is painted.  A null brush will cause the context-fill value to come from
          the <a href="/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_id2d1svgglyphstyle_uint32_d2d1_draw_text_options_dwrite_measuring_mode)">defaultFillBrush</a>. If the defaultFillBrush is also null, the context-fill value will be 'none'.
          To set the ‘context-fill’ value, this method uses the provided brush with its opacity set to 1. To set the ‘context-fill-opacity’ value, this method uses the opacity of the provided brush.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code.

## -see-also

<a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1svgglyphstyle">ID2D1SvgGlyphStyle</a>