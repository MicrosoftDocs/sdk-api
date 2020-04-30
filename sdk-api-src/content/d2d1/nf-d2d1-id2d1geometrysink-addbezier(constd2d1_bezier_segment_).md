---
UID: NF:d2d1.ID2D1GeometrySink.AddBezier(const D2D1_BEZIER_SEGMENT &)
title: ID2D1GeometrySink::AddBezier(const D2D1_BEZIER_SEGMENT &) (d2d1.h)
description: Creates a cubic Bezier curve between the current point and the specified end point.
helpviewer_keywords: ["AddBezier","AddBezier method [Direct2D]","AddBezier method [Direct2D]","ID2D1GeometrySink interface","ID2D1GeometrySink interface [Direct2D]","AddBezier method","ID2D1GeometrySink.AddBezier","ID2D1GeometrySink.AddBezier(const D2D1_BEZIER_SEGMENT &)","ID2D1GeometrySink::AddBezier","ID2D1GeometrySink::AddBezier(const D2D1_BEZIER_SEGMENT &)","d2d1/ID2D1GeometrySink::AddBezier","direct2d.ID2D1GeometrySink_AddBezier_ref_D2D1_BEZIER_SEGMENT"]
old-location: direct2d\ID2D1GeometrySink_AddBezier_ref_D2D1_BEZIER_SEGMENT.htm
tech.root: Direct2D
ms.assetid: f6633960-eff5-4e51-9b08-c8a07c5e11d3
ms.date: 12/05/2018
ms.keywords: AddBezier, AddBezier method [Direct2D], AddBezier method [Direct2D],ID2D1GeometrySink interface, ID2D1GeometrySink interface [Direct2D],AddBezier method, ID2D1GeometrySink.AddBezier, ID2D1GeometrySink.AddBezier(const D2D1_BEZIER_SEGMENT &), ID2D1GeometrySink::AddBezier, ID2D1GeometrySink::AddBezier(const D2D1_BEZIER_SEGMENT &), d2d1/ID2D1GeometrySink::AddBezier, direct2d.ID2D1GeometrySink_AddBezier_ref_D2D1_BEZIER_SEGMENT
f1_keywords:
- d2d1/ID2D1GeometrySink.AddBezier
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- D2d1.dll
api_name:
- ID2D1GeometrySink.AddBezier
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

## -description

Creates a cubic Bezier curve between the current point and the specified end point.

## -parameters

### -param bezier

Type: [in] <b>const <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/ns-d2d1-d2d1_bezier_segment">D2D1_BEZIER_SEGMENT</a> &</b>

A structure that describes the control points and end point of the Bezier curve to add.

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/Direct2D/direct2d-geometries-overview">Geometries Overview</a>

<a href="https://docs.microsoft.com/windows/desktop/Direct2D/how-to-draw-and-fill-a-complex-shape">How to Draw and Fill a Complex Shape</a>

<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1geometrysink">ID2D1GeometrySink</a>