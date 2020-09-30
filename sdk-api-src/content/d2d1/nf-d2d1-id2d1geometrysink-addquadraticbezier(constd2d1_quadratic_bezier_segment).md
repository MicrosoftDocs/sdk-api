---
UID: NF:d2d1.ID2D1GeometrySink.AddQuadraticBezier(constD2D1_QUADRATIC_BEZIER_SEGMENT)
title: ID2D1GeometrySink::AddQuadraticBezier (d2d1.h)
description: Creates a quadratic Bezier curve between the current point and the specified end point and adds it to the geometry sink.
helpviewer_keywords: ["AddQuadraticBezier","AddQuadraticBezier methods [Direct2D]","ID2D1GeometrySink.AddQuadraticBezier","ID2D1GeometrySink::AddQuadraticBezier","d2d1/AddQuadraticBezier","direct2d.id2d1geometrysink_addquadraticbezier"]
old-location: direct2d\id2d1geometrysink_addquadraticbezier.htm
tech.root: Direct2D
ms.assetid: 142f0823-0d8d-4216-8f40-9dec7f48032e
ms.date: 12/05/2018
ms.keywords: AddQuadraticBezier, AddQuadraticBezier methods [Direct2D], ID2D1GeometrySink.AddQuadraticBezier, ID2D1GeometrySink::AddQuadraticBezier, d2d1/AddQuadraticBezier, direct2d.id2d1geometrysink_addquadraticbezier
req.header: d2d1.h
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
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1GeometrySink::AddQuadraticBezier
 - d2d1/ID2D1GeometrySink::AddQuadraticBezier
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - ID2D1GeometrySink::AddQuadraticBezier
---

## -description

Creates a quadratic Bezier curve between the current point and the specified end point.

## -parameters

### -param bezier

Type: [in] <b>const <a href="/windows/win32/api/d2d1/ns-d2d1-d2d1_quadratic_bezier_segment">D2D1_QUADRATIC_BEZIER_SEGMENT</a>*</b>

A structure that describes the control point and the end point of the quadratic Bezier curve to add.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink">ID2D1GeometrySink</a>

