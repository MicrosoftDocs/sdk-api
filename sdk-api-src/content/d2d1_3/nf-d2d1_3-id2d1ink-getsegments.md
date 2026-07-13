---
UID: NF:d2d1_3.ID2D1Ink.GetSegments
title: ID2D1Ink::GetSegments (d2d1_3.h)
description: Retrieves the specified subset of segments stored in this ink object.
helpviewer_keywords: ["GetSegments","GetSegments method [Direct2D]","GetSegments method [Direct2D]","ID2D1Ink interface","ID2D1Ink interface [Direct2D]","GetSegments method","ID2D1Ink.GetSegments","ID2D1Ink::GetSegments","d2d1_3/ID2D1Ink::GetSegments","direct2d.id2d1ink_getsegments"]
old-location: direct2d\id2d1ink_getsegments.htm
tech.root: Direct2D
ms.assetid: 3B6E2823-6F66-4C2F-B8EA-94B03F19DFCD
ms.date: 12/05/2018
ms.keywords: GetSegments, GetSegments method [Direct2D], GetSegments method [Direct2D],ID2D1Ink interface, ID2D1Ink interface [Direct2D],GetSegments method, ID2D1Ink.GetSegments, ID2D1Ink::GetSegments, d2d1_3/ID2D1Ink::GetSegments, direct2d.id2d1ink_getsegments
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
 - ID2D1Ink::GetSegments
 - d2d1_3/ID2D1Ink::GetSegments
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
 - ID2D1Ink.GetSegments
---

# ID2D1Ink::GetSegments


## -description

Retrieves the specified subset of segments stored in this ink object.

## -parameters

### -param startSegment

Type: <b>UINT32</b>

The index of the first segment in this ink object to retrieve.

### -param segments [out]

Type: <b><a href="/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_bezier_segment">D2D1_INK_BEZIER_SEGMENT</a>*</b>

When this method returns, contains a pointer to an array of retrieved segments.

### -param segmentsCount

Type: <b>UINT32</b>

The number of segments to retrieve. Note that segmentsCount must be less than or equal to the number of segments in the ink object minus startSegment.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1ink">ID2D1Ink</a>