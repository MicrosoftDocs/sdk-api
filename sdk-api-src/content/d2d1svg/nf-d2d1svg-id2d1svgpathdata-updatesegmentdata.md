---
UID: NF:d2d1svg.ID2D1SvgPathData.UpdateSegmentData
title: ID2D1SvgPathData::UpdateSegmentData (d2d1svg.h)
description: Updates the segment data array. Existing segment data not updated by this method are preserved. The array is resized larger if necessary to accommodate the new segment data.
helpviewer_keywords: ["ID2D1SvgPathData interface [Direct2D]","UpdateSegmentData method","ID2D1SvgPathData.UpdateSegmentData","ID2D1SvgPathData::UpdateSegmentData","UpdateSegmentData","UpdateSegmentData method [Direct2D]","UpdateSegmentData method [Direct2D]","ID2D1SvgPathData interface","d2d1svg/ID2D1SvgPathData::UpdateSegmentData","direct2d.id2d1svgpathdata_updatesegmentdata"]
old-location: direct2d\id2d1svgpathdata_updatesegmentdata.htm
tech.root: Direct2D
ms.assetid: 3B87B002-7F1C-4531-B584-C0CFC8E46256
ms.date: 12/05/2018
ms.keywords: ID2D1SvgPathData interface [Direct2D],UpdateSegmentData method, ID2D1SvgPathData.UpdateSegmentData, ID2D1SvgPathData::UpdateSegmentData, UpdateSegmentData, UpdateSegmentData method [Direct2D], UpdateSegmentData method [Direct2D],ID2D1SvgPathData interface, d2d1svg/ID2D1SvgPathData::UpdateSegmentData, direct2d.id2d1svgpathdata_updatesegmentdata
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
 - ID2D1SvgPathData::UpdateSegmentData
 - d2d1svg/ID2D1SvgPathData::UpdateSegmentData
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
 - ID2D1SvgPathData.UpdateSegmentData
---

# ID2D1SvgPathData::UpdateSegmentData


## -description

Updates the segment data array. Existing segment data not updated by this method are preserved. 
        The array is resized larger if necessary to accommodate the new segment data.

## -parameters

### -param data [in]

Type: <b>const FLOAT*</b>

The data array.

### -param dataCount

Type: <b>UINT32</b>

The number of data to update.

### -param startIndex

Type: <b>UINT32</b>

The index at which to begin updating segment data. Must be less than or equal to the size of the segment data array.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code.

## -see-also

<a href="/windows/desktop/api/d2d1svg/nn-d2d1svg-id2d1svgpathdata">ID2D1SvgPathData</a>