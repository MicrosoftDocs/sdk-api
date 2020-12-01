---
UID: NF:d2d1svg.ID2D1SvgPathData.GetSegmentData
title: ID2D1SvgPathData::GetSegmentData (d2d1svg.h)
description: Gets data from the segment data array.
helpviewer_keywords: ["GetSegmentData","GetSegmentData method [Direct2D]","GetSegmentData method [Direct2D]","ID2D1SvgPathData interface","ID2D1SvgPathData interface [Direct2D]","GetSegmentData method","ID2D1SvgPathData.GetSegmentData","ID2D1SvgPathData::GetSegmentData","d2d1svg/ID2D1SvgPathData::GetSegmentData","direct2d.id2d1svgpathdata_getsegmentdata"]
old-location: direct2d\id2d1svgpathdata_getsegmentdata.htm
tech.root: Direct2D
ms.assetid: D935BCEB-D7B8-4245-AD1C-25BAE63F8944
ms.date: 12/05/2018
ms.keywords: GetSegmentData, GetSegmentData method [Direct2D], GetSegmentData method [Direct2D],ID2D1SvgPathData interface, ID2D1SvgPathData interface [Direct2D],GetSegmentData method, ID2D1SvgPathData.GetSegmentData, ID2D1SvgPathData::GetSegmentData, d2d1svg/ID2D1SvgPathData::GetSegmentData, direct2d.id2d1svgpathdata_getsegmentdata
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
 - ID2D1SvgPathData::GetSegmentData
 - d2d1svg/ID2D1SvgPathData::GetSegmentData
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
 - ID2D1SvgPathData.GetSegmentData
---

# ID2D1SvgPathData::GetSegmentData


## -description

Gets data from the segment data array.

## -parameters

### -param data [out]

Type: <b>FLOAT*</b>

Buffer to contain the segment data array.

### -param dataCount

Type: <b>UINT32</b>

The element count of the buffer.

### -param startIndex

Type: <b>UINT32</b>

The index of the first segment data to retrieve.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code.

## -see-also

<a href="/windows/desktop/api/d2d1svg/nn-d2d1svg-id2d1svgpathdata">ID2D1SvgPathData</a>