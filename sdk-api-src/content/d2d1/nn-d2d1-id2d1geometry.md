---
UID: NN:d2d1.ID2D1Geometry
title: ID2D1Geometry (d2d1.h)
description: Represents a geometry resource and defines a set of helper methods for manipulating and measuring geometric shapes. Interfaces that inherit from ID2D1Geometry define specific shapes.
helpviewer_keywords: ["ID2D1Geometry","ID2D1Geometry interface [Direct2D]","ID2D1Geometry interface [Direct2D]","described","d2d1/ID2D1Geometry","direct2d.ID2D1Geometry"]
old-location: direct2d\ID2D1Geometry.htm
tech.root: Direct2D
ms.assetid: be4ab801-64f6-48f9-8f62-d0492cc438b1
ms.date: 12/05/2018
ms.keywords: ID2D1Geometry, ID2D1Geometry interface [Direct2D], ID2D1Geometry interface [Direct2D],described, d2d1/ID2D1Geometry, direct2d.ID2D1Geometry
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
 - ID2D1Geometry
 - d2d1/ID2D1Geometry
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
 - ID2D1Geometry
---

# ID2D1Geometry interface


## -description

Represents a geometry resource and defines a set of helper methods for manipulating and measuring geometric shapes.  Interfaces that inherit from <b>ID2D1Geometry</b> define specific shapes.

## -inheritance

The <b>ID2D1Geometry</b> interface inherits from <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1resource">ID2D1Resource</a>. <b>ID2D1Geometry</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

There are several types of Direct2D geometry objects:  a  simple geometry (<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry">ID2D1RectangleGeometry</a>, <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry">ID2D1RoundedRectangleGeometry</a>, or <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry">ID2D1EllipseGeometry</a>), a path geometry (<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry">ID2D1PathGeometry</a>), or a composite geometry (<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup">ID2D1GeometryGroup</a> and <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry">ID2D1TransformedGeometry</a>).

 Direct2D geometries enable you to  describe two-dimensional figures and also offer  many uses, such as defining  hit-test regions,  clip regions, and even   animation paths.

Direct2D geometries are immutable and device-independent resources created by <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1factory">ID2D1Factory</a>.  In general, you should create geometries once and retain them for the life of the application, or until they need to be modified. For more information about device-independent and device-dependent resources, see  the <a href="/windows/win32/Direct2D/resources-and-resource-domains">Resources Overview</a>.

## -see-also

<a href="/windows/win32/Direct2D/geometries">Geometry Overview</a>



<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1resource">ID2D1Resource</a>

