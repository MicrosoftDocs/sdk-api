---
UID: NF:d2d1.ID2D1PathGeometry.Stream
title: ID2D1PathGeometry::Stream (d2d1.h)
description: Copies the contents of the path geometry to the specified ID2D1GeometrySink.
helpviewer_keywords: ["ID2D1PathGeometry interface [Direct2D]","Stream method","ID2D1PathGeometry.Stream","ID2D1PathGeometry::Stream","Stream","Stream method [Direct2D]","Stream method [Direct2D]","ID2D1PathGeometry interface","d2d1/ID2D1PathGeometry::Stream","direct2d.ID2D1PathGeometry_Stream"]
old-location: direct2d\ID2D1PathGeometry_Stream.htm
tech.root: Direct2D
ms.assetid: e128b4e7-8fde-44f1-a7a3-928aace0fe7f
ms.date: 12/05/2018
ms.keywords: ID2D1PathGeometry interface [Direct2D],Stream method, ID2D1PathGeometry.Stream, ID2D1PathGeometry::Stream, Stream, Stream method [Direct2D], Stream method [Direct2D],ID2D1PathGeometry interface, d2d1/ID2D1PathGeometry::Stream, direct2d.ID2D1PathGeometry_Stream
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1PathGeometry::Stream
 - d2d1/ID2D1PathGeometry::Stream
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
 - ID2D1PathGeometry.Stream
---

# ID2D1PathGeometry::Stream


## -description

Copies the contents of the path geometry to the specified <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink">ID2D1GeometrySink</a>.

## -parameters

### -param geometrySink [in]

Type: <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink">ID2D1GeometrySink</a>*</b>

The sink to which the path geometry's contents are copied. Modifying this sink does not change the contents of this path geometry.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry">ID2D1PathGeometry</a>

