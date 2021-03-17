---
UID: NF:d2d1svg.ID2D1SvgPointCollection.GetPoints
title: ID2D1SvgPointCollection::GetPoints (d2d1svg.h)
description: Gets points from the points array.
helpviewer_keywords: ["GetPoints","GetPoints method [Direct2D]","GetPoints method [Direct2D]","ID2D1SvgPointCollection interface","ID2D1SvgPointCollection interface [Direct2D]","GetPoints method","ID2D1SvgPointCollection.GetPoints","ID2D1SvgPointCollection::GetPoints","d2d1svg/ID2D1SvgPointCollection::GetPoints","direct2d.id2d1svgpointcollection_getpoints"]
old-location: direct2d\id2d1svgpointcollection_getpoints.htm
tech.root: Direct2D
ms.assetid: 886039FB-0640-4B20-84E2-4B3EC2AFA234
ms.date: 12/05/2018
ms.keywords: GetPoints, GetPoints method [Direct2D], GetPoints method [Direct2D],ID2D1SvgPointCollection interface, ID2D1SvgPointCollection interface [Direct2D],GetPoints method, ID2D1SvgPointCollection.GetPoints, ID2D1SvgPointCollection::GetPoints, d2d1svg/ID2D1SvgPointCollection::GetPoints, direct2d.id2d1svgpointcollection_getpoints
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
 - ID2D1SvgPointCollection::GetPoints
 - d2d1svg/ID2D1SvgPointCollection::GetPoints
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
 - ID2D1SvgPointCollection.GetPoints
---

# ID2D1SvgPointCollection::GetPoints


## -description

Gets points from the points array.

## -parameters

### -param points [out]

Type: <b>D2D1_POINT_2F*</b>

Buffer to contain the points.

### -param pointsCount

Type: <b>UINT32</b>

The element count of the buffer.

### -param startIndex

Type: <b>UINT32</b>

The index of the first point to retrieve.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code.

## -see-also

<a href="/windows/desktop/api/d2d1svg/nn-d2d1svg-id2d1svgpointcollection">ID2D1SvgPointCollection</a>