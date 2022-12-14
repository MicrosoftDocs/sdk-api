---
UID: NN:d2d1.ID2D1Brush
title: ID2D1Brush (d2d1.h)
description: Defines an object that paints an area. Interfaces that derive from ID2D1Brush describe how the area is painted.
helpviewer_keywords: ["ID2D1Brush","ID2D1Brush interface [Direct2D]","ID2D1Brush interface [Direct2D]","described","d2d1/ID2D1Brush","direct2d.ID2D1Brush"]
old-location: direct2d\ID2D1Brush.htm
tech.root: Direct2D
ms.assetid: 5b8f6ff8-ba52-4d30-9bea-3de89793c868
ms.date: 12/05/2018
ms.keywords: ID2D1Brush, ID2D1Brush interface [Direct2D], ID2D1Brush interface [Direct2D],described, d2d1/ID2D1Brush, direct2d.ID2D1Brush
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
 - ID2D1Brush
 - d2d1/ID2D1Brush
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1.dll
api_name:
 - ID2D1Brush
---

# ID2D1Brush interface


## -description

Defines an object that paints an area. Interfaces that derive from <b>ID2D1Brush</b> describe how the area is painted.

## -inheritance

The <b>ID2D1Brush</b> interface inherits from <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1resource">ID2D1Resource</a>. <b>ID2D1Brush</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

An <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush">ID2D1BitmapBrush</a> is a device-dependent resource: your application should create bitmap brushes after it initializes the render target with which the bitmap brush will be used, and recreate the bitmap brush whenever the render target needs recreated. (For more information about resources, see <a href="/windows/win32/Direct2D/resources-and-resource-domains">Resources Overview</a>.)

Brush space in Direct2D is specified differently than in XPS and Windows Presentation Foundation (WPF). In Direct2D, brush space is not relative to the object being drawn, but rather is the current coordinate system of the render target, transformed by the brush transform, if present. To paint an object as it would be painted by a WPF brush, you must translate the brush space origin to the upper-left corner of the object's bounding box, and then scale the brush space so that the base tile fills the bounding box of the object.

For more information about brushes, see the <a href="/windows/win32/Direct2D/direct2d-brushes-overview">Brushes Overview</a>.

## -see-also

<a href="/windows/win32/Direct2D/direct2d-brushes-overview">Brushes Overview</a>



<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1resource">ID2D1Resource</a>

