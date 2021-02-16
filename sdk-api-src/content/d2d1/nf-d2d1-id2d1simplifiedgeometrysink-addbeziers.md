---
UID: NF:d2d1.ID2D1SimplifiedGeometrySink.AddBeziers
title: ID2D1SimplifiedGeometrySink::AddBeziers (d2d1.h)
description: Creates a sequence of cubic Bezier curves and adds them to the geometry sink.
helpviewer_keywords: ["AddBeziers","AddBeziers method [Direct2D]","AddBeziers method [Direct2D]","ID2D1SimplifiedGeometrySink interface","ID2D1SimplifiedGeometrySink interface [Direct2D]","AddBeziers method","ID2D1SimplifiedGeometrySink.AddBeziers","ID2D1SimplifiedGeometrySink::AddBeziers","d2d1/ID2D1SimplifiedGeometrySink::AddBeziers","direct2d.ID2D1SimplifiedGeometrySink_AddBeziers"]
old-location: direct2d\ID2D1SimplifiedGeometrySink_AddBeziers.htm
tech.root: Direct2D
ms.assetid: 9f079b38-b8ba-40b2-a5ed-4c9732cfd0c6
ms.date: 12/05/2018
ms.keywords: AddBeziers, AddBeziers method [Direct2D], AddBeziers method [Direct2D],ID2D1SimplifiedGeometrySink interface, ID2D1SimplifiedGeometrySink interface [Direct2D],AddBeziers method, ID2D1SimplifiedGeometrySink.AddBeziers, ID2D1SimplifiedGeometrySink::AddBeziers, d2d1/ID2D1SimplifiedGeometrySink::AddBeziers, direct2d.ID2D1SimplifiedGeometrySink_AddBeziers
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
 - ID2D1SimplifiedGeometrySink::AddBeziers
 - d2d1/ID2D1SimplifiedGeometrySink::AddBeziers
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
 - ID2D1SimplifiedGeometrySink.AddBeziers
---

# ID2D1SimplifiedGeometrySink::AddBeziers


## -description

Creates a sequence of cubic Bezier curves and adds them to the geometry sink.

## -parameters

### -param beziers [in]

Type: <b>const <a href="/windows/win32/api/d2d1/ns-d2d1-d2d1_bezier_segment">D2D1_BEZIER_SEGMENT</a>*</b>

A pointer to an array of Bezier segments that describes the Bezier curves to create. A curve is drawn from the geometry sink's current point (the end point of the last segment drawn or the location specified by <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure">BeginFigure</a>) to the end point of the first Bezier segment in the array. if the array contains additional Bezier segments, each subsequent Bezier segment uses the end point of the preceding Bezier segment as its start point.

### -param beziersCount

Type: <b>UINT</b>

The number of Bezier segments in the <i>beziers</i> array.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink">ID2D1SimplifiedGeometrySink</a>

