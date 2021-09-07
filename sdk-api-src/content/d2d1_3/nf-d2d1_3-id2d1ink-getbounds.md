---
UID: NF:d2d1_3.ID2D1Ink.GetBounds
title: ID2D1Ink::GetBounds (d2d1_3.h)
description: Retrieve the bounds of the geometry, with an optional applied transform.
helpviewer_keywords: ["GetBounds","GetBounds method [Direct2D]","GetBounds method [Direct2D]","ID2D1Ink interface","ID2D1Ink interface [Direct2D]","GetBounds method","ID2D1Ink.GetBounds","ID2D1Ink::GetBounds","d2d1_3/ID2D1Ink::GetBounds","direct2d.id2d1ink_getbounds"]
old-location: direct2d\id2d1ink_getbounds.htm
tech.root: Direct2D
ms.assetid: 83BA2631-B3EA-4411-A5F7-265C95A00C9F
ms.date: 12/05/2018
ms.keywords: GetBounds, GetBounds method [Direct2D], GetBounds method [Direct2D],ID2D1Ink interface, ID2D1Ink interface [Direct2D],GetBounds method, ID2D1Ink.GetBounds, ID2D1Ink::GetBounds, d2d1_3/ID2D1Ink::GetBounds, direct2d.id2d1ink_getbounds
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
req.lib: D2d1_3.lib
req.dll: D2d1_3.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1Ink::GetBounds
 - d2d1_3/ID2D1Ink::GetBounds
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1_3.dll
api_name:
 - ID2D1Ink.GetBounds
---

# ID2D1Ink::GetBounds


## -description

Retrieve the bounds of the geometry, with an optional applied transform.

## -parameters

### -param inkStyle [in, optional]

Type: <b><a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1inkstyle">ID2D1InkStyle</a>*</b>

The ink style to be used in determining the bounds of this ink object.

### -param worldTransform [in, optional]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a>*</b>

The world transform to be used in determining the bounds of this ink object.

### -param bounds [out]

Type: <b><a href="/windows/desktop/Direct2D/d2d1-rect-f">D2D1_RECT_F</a>*</b>

When this method returns, contains the bounds of this ink object.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1ink">ID2D1Ink</a>