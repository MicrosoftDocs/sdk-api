---
UID: NN:xpsobjectmodel.IXpsOMGradientBrush
title: IXpsOMGradientBrush (xpsobjectmodel.h)
description: This interface describes a gradient that is made up of gradient stops. Classes that inherit from IXpsOMGradientBrush specify different ways of interpreting gradient stops.
helpviewer_keywords: ["IXpsOMGradientBrush","IXpsOMGradientBrush interface [XPS Documents and Packaging]","IXpsOMGradientBrush interface [XPS Documents and Packaging]","described","xps.ixpsomgradientbrush","xpsobjectmodel/IXpsOMGradientBrush"]
old-location: xps\ixpsomgradientbrush.htm
tech.root: xps
ms.assetid: d381b813-5368-4ffe-a9a1-0f5027ae9d80
ms.date: 12/05/2018
ms.keywords: IXpsOMGradientBrush, IXpsOMGradientBrush interface [XPS Documents and Packaging], IXpsOMGradientBrush interface [XPS Documents and Packaging],described, xps.ixpsomgradientbrush, xpsobjectmodel/IXpsOMGradientBrush
f1_keywords:
- xpsobjectmodel/IXpsOMGradientBrush
dev_langs:
- c++
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- xpsobjectmodel.h
api_name:
- IXpsOMGradientBrush
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMGradientBrush interface


## -description


This interface describes a gradient that is made up of gradient stops. Classes that inherit from <b>IXpsOMGradientBrush</b> specify different ways of interpreting gradient stops.

<b>IXpsOMGradientBrush</b> is the base interface for the <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomlineargradientbrush">IXpsOMLinearGradientBrush</a> and <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush">IXpsOMRadialGradientBrush</a> interfaces.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMGradientBrush</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush">IXpsOMBrush</a>. <b>IXpsOMGradientBrush</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMGradientBrush</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgradientbrush-getcolorinterpolationmode">GetColorInterpolationMode</a>
</td>
<td align="left" width="63%">
Gets the gamma function to be used for color interpolation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgradientbrush-getgradientstops">GetGradientStops</a>
</td>
<td align="left" width="63%">
Gets a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstopcollection">IXpsOMGradientStopCollection</a> interface that contains the collection of <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstop">IXpsOMGradientStop</a> interfaces that define the gradient.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgradientbrush-getspreadmethod">GetSpreadMethod</a>
</td>
<td align="left" width="63%">
Gets the <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_spread_method">XPS_SPREAD_METHOD</a> value, which describes how the area outside of the gradient region will be rendered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgradientbrush-gettransform">GetTransform</a>
</td>
<td align="left" width="63%">
Gets a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform">IXpsOMMatrixTransform</a> interface that contains the resolved matrix transform for the brush.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgradientbrush-gettransformlocal">GetTransformLocal</a>
</td>
<td align="left" width="63%">
Gets a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform">IXpsOMMatrixTransform</a> interface that contains the local, unshared, resolved matrix transform for the brush.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgradientbrush-gettransformlookup">GetTransformLookup</a>
</td>
<td align="left" width="63%">
Gets the name of the lookup key  of the shared matrix transform interface that is to be used for the brush.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgradientbrush-setcolorinterpolationmode">SetColorInterpolationMode</a>
</td>
<td align="left" width="63%">
Sets the <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_color_interpolation">XPS_COLOR_INTERPOLATION</a> value, which describes the gamma function to be used for color interpolation.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgradientbrush-setspreadmethod">SetSpreadMethod</a>
</td>
<td align="left" width="63%">
Sets the <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_spread_method">XPS_SPREAD_METHOD</a> value, which describes how the area outside of the gradient region is to be rendered.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgradientbrush-settransformlocal">SetTransformLocal</a>
</td>
<td align="left" width="63%">
Sets the <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform">IXpsOMMatrixTransform</a> interface pointer to a local, unshared matrix transform that is to be used for the brush.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgradientbrush-settransformlookup">SetTransformLookup</a>
</td>
<td align="left" width="63%">
Sets the name of the lookup key of a shared matrix transform that is to be used for the brush.

</td>
</tr>
</table> 


## -remarks



The methods of this interface define the basic parameters of a gradient. The gradient type, which can be linear or radial,  determines how these parameters are applied.

As shown in the figure that follows, the start and end points of a linear gradient mark the end points of the gradient path. The gradient path is the straight line that connects the start and end points. The gradient region of a linear gradient consists of the area between the start and end points, including those points, and extends in both directions at a right angle to the gradient path. The spread area is the area outside the gradient region.

Gradient stops  define the color at specific locations along the gradient path; the color is interpolated along the gradient path between the gradient stops, as shown in the following illustration.

<img alt="A figure that shows the terms used in a linear gradient" src="./images/LinearGradient1.png"/>
As shown in the figure that follows, the gradient region of a radial gradient is the area enclosed by the ellipse that is described by the center point and the x and y radii that extend from the center point. The spread area is the area outside of that ellipse. The gradient path is a radial line that sweeps the entire gradient region from the gradient origin to the ellipse that bounds the gradient region. In the following illustration, the gradient path is not shown.

<img alt="A figure that shows the terms used in a radial gradient" src="./images/RadialGradient1.png"/>
The spread method describes how the spread area is filled. Implementation of the spread method depends on the gradient type (linear or radial). The following illustration shows several examples of how the spread area can be filled. For  information about different spread methods, see <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_spread_method">XPS_SPREAD_METHOD</a>.

<img alt="An illustration that shows examples of the spread method" src="./images/XPS_Spread_Method.png"/>
 The transform  determines how the resulting gradient is transformed. The visible part of the gradient that is ultimately rendered in the image is determined by the path, stroke, or glyph that is using the gradient brush.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush">IXpsOMBrush</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomlineargradientbrush">IXpsOMLinearGradientBrush</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush">IXpsOMRadialGradientBrush</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd316980(v=vs.85)">Interfaces</a>



<a href="https://www.microsoft.com/download/details.aspx?id=11816">XML Paper Specification</a>
 

 

