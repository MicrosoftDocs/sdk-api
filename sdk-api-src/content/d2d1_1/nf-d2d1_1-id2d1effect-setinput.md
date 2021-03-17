---
UID: NF:d2d1_1.ID2D1Effect.SetInput
title: ID2D1Effect::SetInput (d2d1_1.h)
description: Sets the given input image by index.
helpviewer_keywords: ["ID2D1Effect interface [Direct2D]","SetInput method","ID2D1Effect.SetInput","ID2D1Effect::SetInput","SetInput","SetInput method [Direct2D]","SetInput method [Direct2D]","ID2D1Effect interface","d2d1_1/ID2D1Effect::SetInput","direct2d.id2d1effect_setinput"]
old-location: direct2d\id2d1effect_setinput.htm
tech.root: Direct2D
ms.assetid: 16db95e8-43e7-403c-bce1-dd2f42e81d6a
ms.date: 12/05/2018
ms.keywords: ID2D1Effect interface [Direct2D],SetInput method, ID2D1Effect.SetInput, ID2D1Effect::SetInput, SetInput, SetInput method [Direct2D], SetInput method [Direct2D],ID2D1Effect interface, d2d1_1/ID2D1Effect::SetInput, direct2d.id2d1effect_setinput
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
 - ID2D1Effect::SetInput
 - d2d1_1/ID2D1Effect::SetInput
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
 - ID2D1Effect.SetInput
---

# ID2D1Effect::SetInput


## -description

Sets the given input image by index.

## -parameters

### -param index

Type: <b>UINT32</b>

The index of the image to set.

### -param input [in, optional]

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1image">ID2D1Image</a>*</b>

The input image to set.

### -param invalidate

Type: <b>BOOL</b>

Whether to invalidate the graph at the location of the effect input

## -remarks

If the input index is out of range, the input image is ignored.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect">ID2D1DeviceContext::CreateEffect</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect">ID2D1Effect</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1effect-getoutput">ID2D1Effect::GetOutput</a>



<a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1image">ID2D1Image</a>