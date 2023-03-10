---
UID: NS:d2d1_1.D2D1_POINT_DESCRIPTION
title: D2D1_POINT_DESCRIPTION (d2d1_1.h)
description: Describes a point on a path geometry.
helpviewer_keywords: ["D2D1_POINT_DESCRIPTION","D2D1_POINT_DESCRIPTION structure [Direct2D]","PD2D1_POINT_DESCRIPTION","PD2D1_POINT_DESCRIPTION structure pointer [Direct2D]","d2d1_1/D2D1_POINT_DESCRIPTION","d2d1_1/PD2D1_POINT_DESCRIPTION","direct2d.d2d1_point_description"]
old-location: direct2d\d2d1_point_description.htm
tech.root: Direct2D
ms.assetid: d6e7a4c1-135f-4ffe-91d7-486de8a9338d
ms.date: 12/05/2018
ms.keywords: D2D1_POINT_DESCRIPTION, D2D1_POINT_DESCRIPTION structure [Direct2D], PD2D1_POINT_DESCRIPTION, PD2D1_POINT_DESCRIPTION structure pointer [Direct2D], d2d1_1/D2D1_POINT_DESCRIPTION, d2d1_1/PD2D1_POINT_DESCRIPTION, direct2d.d2d1_point_description
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: D2D1.lib
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D2D1_POINT_DESCRIPTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_POINT_DESCRIPTION
 - d2d1_1/D2D1_POINT_DESCRIPTION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - D2D1.lib
api_name:
 - D2D1_POINT_DESCRIPTION
---

# D2D1_POINT_DESCRIPTION structure


## -description

Describes a point on a path geometry.

## -struct-fields

### -field point

The end point after walking the path.

### -field unitTangentVector

A unit vector indicating the tangent point.

### -field endSegment

The index of the segment on which point resides. This index is global to the entire path, not just to a particular figure.

### -field endFigure

The index of the figure on which point resides.

### -field lengthToEndSegment

The length of the section of the path stretching from the start of the path  to the start of <b>endSegment</b>.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1pathgeometry1-computepointandsegmentatlength(float_uint32_constd2d1_matrix_3x2_f_d2d1_point_description)">ID2D1PathGeometry1::ComputePointAndSegmentAtLength</a>