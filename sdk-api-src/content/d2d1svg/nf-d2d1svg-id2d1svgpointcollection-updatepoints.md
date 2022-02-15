---
UID: NF:d2d1svg.ID2D1SvgPointCollection.UpdatePoints
title: ID2D1SvgPointCollection::UpdatePoints (d2d1svg.h)
description: Updates the points array. Existing points not updated by this method are preserved. The array is resized larger if necessary to accommodate the new points.
helpviewer_keywords: ["ID2D1SvgPointCollection interface [Direct2D]","UpdatePoints method","ID2D1SvgPointCollection.UpdatePoints","ID2D1SvgPointCollection::UpdatePoints","UpdatePoints","UpdatePoints method [Direct2D]","UpdatePoints method [Direct2D]","ID2D1SvgPointCollection interface","d2d1svg/ID2D1SvgPointCollection::UpdatePoints","direct2d.id2d1svgpointcollection_updatepoints"]
old-location: direct2d\id2d1svgpointcollection_updatepoints.htm
tech.root: Direct2D
ms.assetid: D1DE682E-FFB1-4090-BE2A-FED41C1E7170
ms.date: 12/05/2018
ms.keywords: ID2D1SvgPointCollection interface [Direct2D],UpdatePoints method, ID2D1SvgPointCollection.UpdatePoints, ID2D1SvgPointCollection::UpdatePoints, UpdatePoints, UpdatePoints method [Direct2D], UpdatePoints method [Direct2D],ID2D1SvgPointCollection interface, d2d1svg/ID2D1SvgPointCollection::UpdatePoints, direct2d.id2d1svgpointcollection_updatepoints
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
 - ID2D1SvgPointCollection::UpdatePoints
 - d2d1svg/ID2D1SvgPointCollection::UpdatePoints
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
 - ID2D1SvgPointCollection.UpdatePoints
---

# ID2D1SvgPointCollection::UpdatePoints


## -description

Updates the points array. Existing points not updated by this method are preserved. The array is resized larger if necessary to accommodate the new points.

## -parameters

### -param points [in]

Type: <b>const D2D1_POINT_2F*</b>

The points array.

### -param pointsCount

Type: <b>UINT32</b>

The number of points to update.

### -param startIndex

Type: <b>UINT32</b>

The index at which to begin updating points. Must be less than or equal to the size of the array.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code.

## -see-also

<a href="/windows/desktop/api/d2d1svg/nn-d2d1svg-id2d1svgpointcollection">ID2D1SvgPointCollection</a>