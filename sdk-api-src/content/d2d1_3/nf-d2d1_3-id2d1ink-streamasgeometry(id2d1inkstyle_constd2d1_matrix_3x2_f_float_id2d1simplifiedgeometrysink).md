---
UID: NF:d2d1_3.ID2D1Ink.StreamAsGeometry(ID2D1InkStyle,constD2D1_MATRIX_3X2_F,FLOAT,ID2D1SimplifiedGeometrySink)
title: ID2D1Ink::StreamAsGeometry (d2d1_3.h)
description: Retrieves a geometric representation of this ink object. (overload 2/4)
helpviewer_keywords: ["ID2D1Ink interface [Direct2D]","StreamAsGeometry method","ID2D1Ink.StreamAsGeometry","ID2D1Ink::StreamAsGeometry","ID2D1Ink::StreamAsGeometry(ID2D1InkStyle","const D2D1_MATRIX_3X2_F","FLOAT","ID2D1SimplifiedGeometrySink)","StreamAsGeometry","StreamAsGeometry method [Direct2D]","StreamAsGeometry method [Direct2D]","ID2D1Ink interface","d2d1_3/ID2D1Ink::StreamAsGeometry","direct2d.id2d1ink_streamasgeometry"]
old-location: direct2d\id2d1ink_streamasgeometry.htm
tech.root: Direct2D
ms.assetid: 385A4C6F-69D9-46A2-ABA4-9E1AA77D6CF4
ms.date: 12/05/2018
ms.keywords: ID2D1Ink interface [Direct2D],StreamAsGeometry method, ID2D1Ink.StreamAsGeometry, ID2D1Ink::StreamAsGeometry, ID2D1Ink::StreamAsGeometry(ID2D1InkStyle,const D2D1_MATRIX_3X2_F,FLOAT,ID2D1SimplifiedGeometrySink), StreamAsGeometry, StreamAsGeometry method [Direct2D], StreamAsGeometry method [Direct2D],ID2D1Ink interface, d2d1_3/ID2D1Ink::StreamAsGeometry, direct2d.id2d1ink_streamasgeometry
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
 - ID2D1Ink::StreamAsGeometry
 - d2d1_3/ID2D1Ink::StreamAsGeometry
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
 - ID2D1Ink.StreamAsGeometry
---

# ID2D1Ink::StreamAsGeometry


## -description

Retrieves a geometric representation of this ink object.

## -parameters

### -param inkStyle [in, optional]

Type: <b><a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1inkstyle">ID2D1InkStyle</a>*</b>

The ink style to be used in determining the geometric representation.

### -param worldTransform [in, optional]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a>*</b>

The world transform to be used in determining the geometric representation.

### -param flatteningTolerance

Type: <b>FLOAT</b>

The flattening tolerance to be used in determining the geometric representation.

### -param geometrySink [in]

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink">ID2D1SimplifiedGeometrySink</a>*</b>

The geometry sink to which the geometry representation will be streamed.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1ink">ID2D1Ink</a>
