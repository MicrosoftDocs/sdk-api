---
UID: NF:d2d1_3.ID2D1Ink.SetSegments
title: ID2D1Ink::SetSegments (d2d1_3.h)
description: Updates the specified segments in this ink object with new control points.
helpviewer_keywords: ["ID2D1Ink interface [Direct2D]","SetSegments method","ID2D1Ink.SetSegments","ID2D1Ink::SetSegments","SetSegments","SetSegments method [Direct2D]","SetSegments method [Direct2D]","ID2D1Ink interface","d2d1_3/ID2D1Ink::SetSegments","direct2d.id2d1ink_setsegments"]
old-location: direct2d\id2d1ink_setsegments.htm
tech.root: Direct2D
ms.assetid: 930D9772-D922-4CEB-A97C-06F263543D81
ms.date: 12/05/2018
ms.keywords: ID2D1Ink interface [Direct2D],SetSegments method, ID2D1Ink.SetSegments, ID2D1Ink::SetSegments, SetSegments, SetSegments method [Direct2D], SetSegments method [Direct2D],ID2D1Ink interface, d2d1_3/ID2D1Ink::SetSegments, direct2d.id2d1ink_setsegments
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
 - ID2D1Ink::SetSegments
 - d2d1_3/ID2D1Ink::SetSegments
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
 - ID2D1Ink.SetSegments
---

# ID2D1Ink::SetSegments


## -description

Updates the specified segments in this ink object with new control points.

## -parameters

### -param startSegment

Type: <b>UINT32</b>

The index of the first segment in this ink object to update.

### -param segments [in]

Type: <b>const <a href="/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_bezier_segment">D2D1_INK_BEZIER_SEGMENT</a>*</b>

A pointer to the array of segment data to be used in the update.

### -param segmentsCount

Type: <b>UINT32</b>

The number of segments in this ink object that will be updated with new data. Note that segmentsCount must be less than or equal to the number of segments in the ink object minus startSegment.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1ink">ID2D1Ink</a>