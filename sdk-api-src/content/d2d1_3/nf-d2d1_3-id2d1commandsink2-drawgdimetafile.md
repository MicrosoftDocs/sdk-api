---
UID: NF:d2d1_3.ID2D1CommandSink2.DrawGdiMetafile
title: ID2D1CommandSink2::DrawGdiMetafile (d2d1_3.h)
description: Draws a metafile to the command sink using the given source and destination rectangles.
helpviewer_keywords: ["DrawGdiMetafile","DrawGdiMetafile method [Direct2D]","DrawGdiMetafile method [Direct2D]","ID2D1CommandSink2 interface","ID2D1CommandSink2 interface [Direct2D]","DrawGdiMetafile method","ID2D1CommandSink2.DrawGdiMetafile","ID2D1CommandSink2::DrawGdiMetafile","d2d1_3/ID2D1CommandSink2::DrawGdiMetafile","direct2d.id2d1commandsink2_drawgdimetafile"]
old-location: direct2d\id2d1commandsink2_drawgdimetafile.htm
tech.root: Direct2D
ms.assetid: ecd1fb9e-0062-c1aa-8275-47b7453bc9ad
ms.date: 12/05/2018
ms.keywords: DrawGdiMetafile, DrawGdiMetafile method [Direct2D], DrawGdiMetafile method [Direct2D],ID2D1CommandSink2 interface, ID2D1CommandSink2 interface [Direct2D],DrawGdiMetafile method, ID2D1CommandSink2.DrawGdiMetafile, ID2D1CommandSink2::DrawGdiMetafile, d2d1_3/ID2D1CommandSink2::DrawGdiMetafile, direct2d.id2d1commandsink2_drawgdimetafile
req.header: d2d1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
 - ID2D1CommandSink2::DrawGdiMetafile
 - d2d1_3/ID2D1CommandSink2::DrawGdiMetafile
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
 - ID2D1CommandSink2.DrawGdiMetafile
---

# ID2D1CommandSink2::DrawGdiMetafile


## -description

Draws a metafile to the command sink using the given source and destination rectangles.

## -parameters

### -param gdiMetafile [in]

Type: <b><a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1gdimetafile">ID2D1GdiMetafile</a>*</b>

The metafile to draw.

### -param destinationRectangle [in]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-rect-f">D2D1_RECT_F</a>*</b>

The rectangle in the target where the metafile will be drawn, relative to the upper left corner (defined in DIPs). If NULL is specified, the destination rectangle is the size of the target.

### -param sourceRectangle [in]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-rect-f">D2D1_RECT_F</a>*</b>

The rectangle of the source metafile that will be drawn, relative to the upper left corner (defined in DIPs). 
     If NULL is specified, the source rectangle is the value returned by <a href="/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1gdimetafile1-getsourcebounds">ID2D1GdiMetafile1::GetSourceBounds</a>.

## -returns

This method does not return a value.

## -see-also

<a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1commandsink2">ID2D1CommandSink2</a>