---
UID: NF:d2d1_3.ID2D1DeviceContext2.DrawInk
title: ID2D1DeviceContext2::DrawInk (d2d1_3.h)
description: Renders the given ink object using the given brush and ink style. (ID2D1DeviceContext2.DrawInk)
helpviewer_keywords: ["DrawInk","DrawInk method [Direct2D]","DrawInk method [Direct2D]","ID2D1DeviceContext2 interface","ID2D1DeviceContext2 interface [Direct2D]","DrawInk method","ID2D1DeviceContext2.DrawInk","ID2D1DeviceContext2::DrawInk","d2d1_3/ID2D1DeviceContext2::DrawInk","direct2d.id2d1devicecontext2_drawink"]
old-location: direct2d\id2d1devicecontext2_drawink.htm
tech.root: Direct2D
ms.assetid: d7c27267-c0c3-d21c-7980-3d92396509c7
ms.date: 12/05/2018
ms.keywords: DrawInk, DrawInk method [Direct2D], DrawInk method [Direct2D],ID2D1DeviceContext2 interface, ID2D1DeviceContext2 interface [Direct2D],DrawInk method, ID2D1DeviceContext2.DrawInk, ID2D1DeviceContext2::DrawInk, d2d1_3/ID2D1DeviceContext2::DrawInk, direct2d.id2d1devicecontext2_drawink
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
 - ID2D1DeviceContext2::DrawInk
 - d2d1_3/ID2D1DeviceContext2::DrawInk
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
 - ID2D1DeviceContext2.DrawInk
---

# ID2D1DeviceContext2::DrawInk


## -description

Renders the given ink object using the given brush and ink style.

## -parameters

### -param ink [in]

Type: <b><a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1ink">ID2D1Ink</a>*</b>

The ink object to be rendered.

### -param brush [in]

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>*</b>

The brush with which to render the ink object.

### -param inkStyle [in, optional]

Type: <b><a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1inkstyle">ID2D1InkStyle</a>*</b>

The ink style to use when rendering the ink object.

## -see-also

<a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1devicecontext2">ID2D1DeviceContext2</a>
