---
UID: NF:d2d1_3.ID2D1Ink.SetSegmentAtEnd(constD2D1_INK_BEZIER_SEGMENT&)
title: ID2D1Ink::SetSegmentAtEnd(const D2D1_INK_BEZIER_SEGMENT &) (d2d1_3.h)
description: Updates the last segment in this ink object with new control points. (overload 2/2)
helpviewer_keywords: ["ID2D1Ink interface [Direct2D]","SetSegmentAtEnd method","ID2D1Ink.SetSegmentAtEnd","ID2D1Ink.SetSegmentAtEnd(const D2D1_INK_BEZIER_SEGMENT &)","ID2D1Ink::SetSegmentAtEnd","ID2D1Ink::SetSegmentAtEnd(const D2D1_INK_BEZIER_SEGMENT &)","SetSegmentAtEnd","SetSegmentAtEnd method [Direct2D]","SetSegmentAtEnd method [Direct2D]","ID2D1Ink interface","d2d1_3/ID2D1Ink::SetSegmentAtEnd","direct2d.id2d1ink_setsegmentatend_2"]
old-location: direct2d\id2d1ink_setsegmentatend_2.htm
tech.root: Direct2D
ms.assetid: C9DB6A07-4FDD-4B39-8D30-DF6453D1E61C
ms.date: 12/05/2018
ms.keywords: ID2D1Ink interface [Direct2D],SetSegmentAtEnd method, ID2D1Ink.SetSegmentAtEnd, ID2D1Ink.SetSegmentAtEnd(const D2D1_INK_BEZIER_SEGMENT &), ID2D1Ink::SetSegmentAtEnd, ID2D1Ink::SetSegmentAtEnd(const D2D1_INK_BEZIER_SEGMENT &), SetSegmentAtEnd, SetSegmentAtEnd method [Direct2D], SetSegmentAtEnd method [Direct2D],ID2D1Ink interface, d2d1_3/ID2D1Ink::SetSegmentAtEnd, direct2d.id2d1ink_setsegmentatend_2
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
 - ID2D1Ink::SetSegmentAtEnd
 - d2d1_3/ID2D1Ink::SetSegmentAtEnd
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
 - ID2D1Ink.SetSegmentAtEnd
---

# ID2D1Ink::SetSegmentAtEnd(const D2D1_INK_BEZIER_SEGMENT &)


## -description

Updates the last segment in this ink object with new control points.

## -parameters

### -param segment [ref]

Type: <b>const <a href="/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_bezier_segment">D2D1_INK_BEZIER_SEGMENT</a></b>

A pointer to the segment data with which to overwrite this ink object's last segment.  Note that if there are currently no segments in the ink object, SetSegmentsAtEnd will return an error.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1ink">ID2D1Ink</a>
