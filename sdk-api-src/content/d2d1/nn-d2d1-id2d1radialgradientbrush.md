---
UID: NN:d2d1.ID2D1RadialGradientBrush
title: ID2D1RadialGradientBrush (d2d1.h)
description: Paints an area with a radial gradient.helpviewer_keywords: ["ID2D1RadialGradientBrush","ID2D1RadialGradientBrush interface [Direct2D]","ID2D1RadialGradientBrush interface [Direct2D]","described","d2d1/ID2D1RadialGradientBrush","direct2d.ID2D1RadialGradientBrush"]
old-location: direct2d\ID2D1RadialGradientBrush.htm
tech.root: Direct2D
ms.assetid: 21ed2286-e4df-4b77-ba31-e5d5927e16f5
ms.date: 12/05/2018
ms.keywords: ID2D1RadialGradientBrush, ID2D1RadialGradientBrush interface [Direct2D], ID2D1RadialGradientBrush interface [Direct2D],described, d2d1/ID2D1RadialGradientBrush, direct2d.ID2D1RadialGradientBrush
f1_keywords:
- d2d1/ID2D1RadialGradientBrush
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
- ID2D1RadialGradientBrush
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1RadialGradientBrush interface


## -description


Paints an area with a radial gradient.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1RadialGradientBrush</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>. <b>ID2D1RadialGradientBrush</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1RadialGradientBrush</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1radialgradientbrush-getcenter">GetCenter</a>
</td>
<td align="left" width="63%">
Retrieves the center of the gradient ellipse. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1radialgradientbrush-getgradientoriginoffset">GetGradientOriginOffset</a>
</td>
<td align="left" width="63%">
Retrieves the offset of the gradient origin relative to the gradient ellipse's center.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1radialgradientbrush-getgradientstopcollection">GetGradientStopCollection</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1gradientstopcollection">ID2D1GradientStopCollection</a> associated with this radial gradient brush object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1radialgradientbrush-getradiusx">GetRadiusX</a>
</td>
<td align="left" width="63%">
Retrieves the x-radius of the gradient ellipse.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1radialgradientbrush-getradiusy">GetRadiusY</a>
</td>
<td align="left" width="63%">
Retrieves the y-radius of the gradient ellipse.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1radialgradientbrush-setcenter">SetCenter</a>
</td>
<td align="left" width="63%">
Specifies the center of the gradient ellipse in the brush's coordinate space. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1radialgradientbrush-setgradientoriginoffset">SetGradientOriginOffset</a>
</td>
<td align="left" width="63%">
Specifies the offset of the gradient origin relative to the gradient ellipse's center.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1radialgradientbrush-setradiusx">SetRadiusX</a>
</td>
<td align="left" width="63%">
Specifies the x-radius of the gradient ellipse, in the brush's coordinate space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1radialgradientbrush-setradiusy">SetRadiusY</a>
</td>
<td align="left" width="63%">
Specifies the y-radius of the gradient ellipse, in the brush's coordinate space.

</td>
</tr>
</table> 


## -remarks



The <b>ID2D1RadialGradientBrush</b> is similar to the <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1lineargradientbrush">ID2D1LinearGradientBrush</a> in that they both map a collection of gradient stops to a gradient. However, the linear gradient has a start and an end point to define the gradient vector, while the radial gradient uses an ellipse and a gradient origin to define its gradient behavior. To define the position and size of the ellipse, use the <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1radialgradientbrush-setcenter">SetCenter</a>, <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1radialgradientbrush-setradiusx">SetRadiusX</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1radialgradientbrush-setradiusy">SetRadiusY</a> methods to specify the center, x-radius, and y-radius of the ellipse. The gradient origin is the center of the ellipse, unless a gradient offset is specified by using the <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1radialgradientbrush-setgradientoriginoffset">SetGradientOriginOffset</a> method.

The brush maps the gradient stop position 0.0f of the gradient origin, and the position 1.0f is mapped to the ellipse boundary. When the gradient origin is within the ellipse, the contents of the ellipse enclose the entire [0, 1] range of the brush gradient stops. If the gradient origin is outside the bounds of the ellipse, the brush still works, but its gradient is not well-defined.

The start point and end point are described in the brush space and are mappped to the render target when the brush is used. Note the starting and ending coordinates are absolute, not relative to the render target size. A value of (0, 0) maps to the upper-left corner of the render target, while a value of (1, 1) maps just one pixel diagonally away from (0, 0). If there is a nonidentity brush transform or render target transform, the brush ellipse and gradient origin are also transformed.

It is possible to specify an ellipse that does not completely fill area being painted. When this occurs,       the            <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode">D2D1_EXTEND_MODE</a> and  setting (specified by the  brush     <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1gradientstopcollection">ID2D1GradientStopCollection</a>) determines how the remaining area is painted. 


<h3><a id="Creating_ID2D1RadialGradientBrush_Objects"></a><a id="creating_id2d1radialgradientbrush_objects"></a><a id="CREATING_ID2D1RADIALGRADIENTBRUSH_OBJECTS"></a>Creating ID2D1RadialGradientBrush Objects</h3>
To create a radial gradient brush, use the <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush)">ID2D1RenderTarget::CreateRadialGradientBrush</a> method of the render target on which the brush will be used. The brush may be used only with the render target that created it or with the compatible targets for that render target.

A radial gradient brush is a device-dependent resource: your application should create radial gradient brushes after it initializes the render target with which the brushes will be used, and recreate the brushes whenever the render target needs recreated. (For more information about resources, see <a href="https://docs.microsoft.com/windows/desktop/Direct2D/resources-and-resource-domains">Resources Overview</a>.)


## Examples

For an example on how to create a radial gradient brush, see the <a href="https://docs.microsoft.com/windows/desktop/Direct2D/how-to-create-a-radial-gradient-brush">How to Create a Radial Gradient Brush</a> topic. 

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Direct2D/direct2d-brushes-overview">Brushes Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/Direct2D/how-to-create-a-radial-gradient-brush">How to Create a Radial Gradient Brush</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>
 

 

