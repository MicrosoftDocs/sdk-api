---
UID: NN:d2d1.ID2D1EllipseGeometry
title: ID2D1EllipseGeometry (d2d1.h)
description: Represents an ellipse.
helpviewer_keywords: ["ID2D1EllipseGeometry","ID2D1EllipseGeometry interface [Direct2D]","ID2D1EllipseGeometry interface [Direct2D]","described","d2d1/ID2D1EllipseGeometry","direct2d.ID2D1EllipseGeometry"]
old-location: direct2d\ID2D1EllipseGeometry.htm
tech.root: Direct2D
ms.assetid: 4ab6452c-6df8-46c0-9e0d-0cebc19d84ba
ms.date: 12/05/2018
ms.keywords: ID2D1EllipseGeometry, ID2D1EllipseGeometry interface [Direct2D], ID2D1EllipseGeometry interface [Direct2D],described, d2d1/ID2D1EllipseGeometry, direct2d.ID2D1EllipseGeometry
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
 - ID2D1EllipseGeometry
 - d2d1/ID2D1EllipseGeometry
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
 - ID2D1EllipseGeometry
---

# ID2D1EllipseGeometry interface


## -description

Represents an ellipse.

## -inheritance

The <b>ID2D1EllipseGeometry</b> interface inherits from <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1geometry">ID2D1Geometry</a>. <b>ID2D1EllipseGeometry</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

<h3><a id="Creating_ID2D1EllipseGeometry_Objects"></a><a id="creating_id2d1ellipsegeometry_objects"></a><a id="CREATING_ID2D1ELLIPSEGEOMETRY_OBJECTS"></a>Creating ID2D1EllipseGeometry Objects</h3>
To create an ellipse geometry, use the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createellipsegeometry(constd2d1_ellipse_id2d1ellipsegeometry)">ID2D1Factory::CreateEllipseGeometry</a> method.

Direct2D geometries are immutable and device-independent resources created by <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1factory">ID2D1Factory</a>.  In general, you should create geometries once and retain them for the life of the application, or until they need to be modified. For more information about device-independent and device-dependent resources, see  the <a href="/windows/win32/Direct2D/resources-and-resource-domains">Resources Overview</a>.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1geometry">ID2D1Geometry</a>

