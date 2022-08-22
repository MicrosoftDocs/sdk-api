---
UID: NF:d2d1_1.ID2D1CommandSink.DrawGdiMetafile
title: ID2D1CommandSink::DrawGdiMetafile (d2d1_1.h)
description: Draw a metafile to the device context. (ID2D1CommandSink.DrawGdiMetafile)
helpviewer_keywords: ["DrawGdiMetafile","DrawGdiMetafile method [Direct2D]","DrawGdiMetafile method [Direct2D]","ID2D1CommandSink interface","ID2D1CommandSink interface [Direct2D]","DrawGdiMetafile method","ID2D1CommandSink.DrawGdiMetafile","ID2D1CommandSink::DrawGdiMetafile","d2d1_1/ID2D1CommandSink::DrawGdiMetafile","direct2d.id2d1commandsink_drawmetafile"]
old-location: direct2d\id2d1commandsink_drawmetafile.htm
tech.root: Direct2D
ms.assetid: 5D986C99-BB7D-4A46-A147-E907F1031E92
ms.date: 12/05/2018
ms.keywords: DrawGdiMetafile, DrawGdiMetafile method [Direct2D], DrawGdiMetafile method [Direct2D],ID2D1CommandSink interface, ID2D1CommandSink interface [Direct2D],DrawGdiMetafile method, ID2D1CommandSink.DrawGdiMetafile, ID2D1CommandSink::DrawGdiMetafile, d2d1_1/ID2D1CommandSink::DrawGdiMetafile, direct2d.id2d1commandsink_drawmetafile
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - ID2D1CommandSink::DrawGdiMetafile
 - d2d1_1/ID2D1CommandSink::DrawGdiMetafile
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
 - ID2D1CommandSink.DrawGdiMetafile
---

# ID2D1CommandSink::DrawGdiMetafile


## -description

Draw a metafile to the device context.

## -parameters

### -param gdiMetafile [in]

Type: <b><a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1gdimetafile">ID2D1GdiMetafile</a>*</b>

The metafile to draw.

### -param targetOffset [in, optional]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a>*</b>

The offset from the upper left corner of the render target.

## -returns

This method does not return a value.

## -remarks

The <i>targetOffset</i> defines the offset in the destination space that the image will be rendered to. The entire logical extent of the image is rendered to the corresponding destination. If you don't specify the offset, the destination origin will be (0, 0). The top, left corner of the image will be mapped to the target offset. This will not necessarily be the origin.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1commandsink">ID2D1CommandSink</a>
