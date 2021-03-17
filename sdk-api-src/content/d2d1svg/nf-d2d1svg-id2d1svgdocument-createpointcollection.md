---
UID: NF:d2d1svg.ID2D1SvgDocument.CreatePointCollection
title: ID2D1SvgDocument::CreatePointCollection (d2d1svg.h)
description: Creates a points object which can be used to set a points attribute on a polygon or polyline element.
helpviewer_keywords: ["CreatePointCollection","CreatePointCollection method [Direct2D]","CreatePointCollection method [Direct2D]","ID2D1SvgDocument interface","ID2D1SvgDocument interface [Direct2D]","CreatePointCollection method","ID2D1SvgDocument.CreatePointCollection","ID2D1SvgDocument::CreatePointCollection","d2d1svg/ID2D1SvgDocument::CreatePointCollection","direct2d.id2d1svgdocument_createpointcollection"]
old-location: direct2d\id2d1svgdocument_createpointcollection.htm
tech.root: Direct2D
ms.assetid: A7AB02F2-32B0-4FF5-8A3A-CE7A6AD9DB57
ms.date: 12/05/2018
ms.keywords: CreatePointCollection, CreatePointCollection method [Direct2D], CreatePointCollection method [Direct2D],ID2D1SvgDocument interface, ID2D1SvgDocument interface [Direct2D],CreatePointCollection method, ID2D1SvgDocument.CreatePointCollection, ID2D1SvgDocument::CreatePointCollection, d2d1svg/ID2D1SvgDocument::CreatePointCollection, direct2d.id2d1svgdocument_createpointcollection
req.header: d2d1svg.h
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
req.dll: Direct2d.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1SvgDocument::CreatePointCollection
 - d2d1svg/ID2D1SvgDocument::CreatePointCollection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - direct2d.dll
api_name:
 - ID2D1SvgDocument.CreatePointCollection
---

# ID2D1SvgDocument::CreatePointCollection


## -description

Creates a points object which can be used to set a points attribute on a polygon or polyline element.

## -parameters

### -param points [in, optional]

Type: <b>const D2D1_POINT_2F*</b>

The points in the point collection.

### -param pointsCount

Type: <b>UINT32</b>

The number of points in the points argument.

### -param pointCollection [out]

Type: <b>ID2D1SvgPointCollection**</b>

The created <a href="/windows/desktop/api/d2d1svg/nn-d2d1svg-id2d1svgpointcollection">ID2D1SvgPointCollection</a> object.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code.

## -see-also

<a href="/windows/desktop/api/d2d1svg/nn-d2d1svg-id2d1svgdocument">ID2D1SvgDocument</a>