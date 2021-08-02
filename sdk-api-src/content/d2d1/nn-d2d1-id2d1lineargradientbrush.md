---
UID: NN:d2d1.ID2D1LinearGradientBrush
title: ID2D1LinearGradientBrush (d2d1.h)
description: Paints an area with a linear gradient.
helpviewer_keywords: ["ID2D1LinearGradientBrush","ID2D1LinearGradientBrush interface [Direct2D]","ID2D1LinearGradientBrush interface [Direct2D]","described","d2d1/ID2D1LinearGradientBrush","direct2d.ID2D1LinearGradientBrush"]
old-location: direct2d\ID2D1LinearGradientBrush.htm
tech.root: Direct2D
ms.assetid: bbb5e36a-d13d-448e-8686-d14ee99b1ccb
ms.date: 12/05/2018
ms.keywords: ID2D1LinearGradientBrush, ID2D1LinearGradientBrush interface [Direct2D], ID2D1LinearGradientBrush interface [Direct2D],described, d2d1/ID2D1LinearGradientBrush, direct2d.ID2D1LinearGradientBrush
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
 - ID2D1LinearGradientBrush
 - d2d1/ID2D1LinearGradientBrush
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
 - ID2D1LinearGradientBrush
---

# ID2D1LinearGradientBrush interface


## -description

Paints an area with a linear gradient.

## -inheritance

The <b>ID2D1LinearGradientBrush</b> interface inherits from <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>. <b>ID2D1LinearGradientBrush</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

An <b>ID2D1LinearGradientBrush</b> paints an area with a linear gradient along a line between the brush start point and end   point. The gradient, defined by the brush <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection">ID2D1GradientStopCollection</a>, is extruded perpendicular to this line, and then transformed by a brush transform (if specified).  

The start point and end point are described in the brush space and are mapped to the render target when the brush is used. Note the starting and ending coordinates are absolute, not relative to the render target size. A value of (0, 0) maps to the upper-left corner of the render target, while a value of (1, 1) maps one pixel diagonally away from (0, 0). If there is a nonidentity brush transform or render target transform, the brush start point and end point are also transformed.  

It is possible to specify a gradient axis that does not completely fill the area that is being painted. When this occurs, the <a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode">D2D1_EXTEND_MODE</a>, specified by the   <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection">ID2D1GradientStopCollection</a>, determines how the remaining area is painted. 


<h3><a id="Creating_ID2D1LinearGradientBrush_Objects"></a><a id="creating_id2d1lineargradientbrush_objects"></a><a id="CREATING_ID2D1LINEARGRADIENTBRUSH_OBJECTS"></a>Creating ID2D1LinearGradientBrush Objects</h3>
To create a linear gradient brush, use the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)">ID2D1RenderTarget::CreateLinearGradientBrush</a> method of the render target on which the brush will be used. The brush can only be used with the render target that created it or with  the compatible targets for that render target.

A linear gradient brush is a device-dependent resource: your application should create linear gradient brushes after it initializes the render target with which the brushes will be used, and recreate the brushes whenever the render target needs recreated. (For more information about resources, see <a href="/windows/win32/Direct2D/resources-and-resource-domains">Resources Overview</a>.)

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>
