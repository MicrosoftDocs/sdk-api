---
UID: NF:d2d1_3.ID2D1CommandSink4.SetPrimitiveBlend2
title: ID2D1CommandSink4::SetPrimitiveBlend2 (d2d1_3.h)
description: Sets a new primitive blend mode. Allows access to the MAX primitive blend mode.
helpviewer_keywords: ["ID2D1CommandSink4 interface [Direct2D]","SetPrimitiveBlend2 method","ID2D1CommandSink4.SetPrimitiveBlend2","ID2D1CommandSink4::SetPrimitiveBlend2","SetPrimitiveBlend2","SetPrimitiveBlend2 method [Direct2D]","SetPrimitiveBlend2 method [Direct2D]","ID2D1CommandSink4 interface","d2d1_3/ID2D1CommandSink4::SetPrimitiveBlend2","direct2d.id2d1commandsink4_setprimitiveblend2"]
old-location: direct2d\id2d1commandsink4_setprimitiveblend2.htm
tech.root: Direct2D
ms.assetid: 20934CEA-2B89-45F5-8E61-CD47C4A9B78F
ms.date: 12/05/2018
ms.keywords: ID2D1CommandSink4 interface [Direct2D],SetPrimitiveBlend2 method, ID2D1CommandSink4.SetPrimitiveBlend2, ID2D1CommandSink4::SetPrimitiveBlend2, SetPrimitiveBlend2, SetPrimitiveBlend2 method [Direct2D], SetPrimitiveBlend2 method [Direct2D],ID2D1CommandSink4 interface, d2d1_3/ID2D1CommandSink4::SetPrimitiveBlend2, direct2d.id2d1commandsink4_setprimitiveblend2
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
 - ID2D1CommandSink4::SetPrimitiveBlend2
 - d2d1_3/ID2D1CommandSink4::SetPrimitiveBlend2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1.dll
api_name:
 - ID2D1CommandSink4.SetPrimitiveBlend2
---

# ID2D1CommandSink4::SetPrimitiveBlend2


## -description

Sets a new primitive blend mode. Allows access to the MAX primitive blend mode.

## -parameters

### -param primitiveBlend

Type: <b><a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_primitive_blend">D2D1_PRIMITIVE_BLEND</a></b>

The primitive blend that will apply to subsequent primitives.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, it returns S_OK. If it fails, it returns an HRESULT error code.

## -see-also

<a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1commandsink4">ID2D1CommandSink4</a>