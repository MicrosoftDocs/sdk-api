---
UID: NF:d2d1_1.ID2D1CommandSink.SetPrimitiveBlend
title: ID2D1CommandSink::SetPrimitiveBlend (d2d1_1.h)
description: Sets a new primitive blend mode. (ID2D1CommandSink.SetPrimitiveBlend)
helpviewer_keywords: ["ID2D1CommandSink interface [Direct2D]","SetPrimitiveBlend method","ID2D1CommandSink.SetPrimitiveBlend","ID2D1CommandSink::SetPrimitiveBlend","SetPrimitiveBlend","SetPrimitiveBlend method [Direct2D]","SetPrimitiveBlend method [Direct2D]","ID2D1CommandSink interface","d2d1_1/ID2D1CommandSink::SetPrimitiveBlend","direct2d.id2d1commandsink_setprimitiveblend"]
old-location: direct2d\id2d1commandsink_setprimitiveblend.htm
tech.root: Direct2D
ms.assetid: 80b7047f-1200-4dc9-bc64-96678524a449
ms.date: 12/05/2018
ms.keywords: ID2D1CommandSink interface [Direct2D],SetPrimitiveBlend method, ID2D1CommandSink.SetPrimitiveBlend, ID2D1CommandSink::SetPrimitiveBlend, SetPrimitiveBlend, SetPrimitiveBlend method [Direct2D], SetPrimitiveBlend method [Direct2D],ID2D1CommandSink interface, d2d1_1/ID2D1CommandSink::SetPrimitiveBlend, direct2d.id2d1commandsink_setprimitiveblend
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
 - ID2D1CommandSink::SetPrimitiveBlend
 - d2d1_1/ID2D1CommandSink::SetPrimitiveBlend
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
 - ID2D1CommandSink.SetPrimitiveBlend
---

# ID2D1CommandSink::SetPrimitiveBlend


## -description

Sets a new primitive blend mode.

## -parameters

### -param primitiveBlend

Type: <b><a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_primitive_blend">D2D1_PRIMITIVE_BLEND</a></b>

The primitive blend that will apply to subsequent primitives.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandlist-stream">ID2D1CommandList::Stream</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1commandsink">ID2D1CommandSink</a>



<a href="/windows/desktop/Direct2D/id2d1rendertarget-settransform">ID2D1RenderTarget::SetTransform</a>
