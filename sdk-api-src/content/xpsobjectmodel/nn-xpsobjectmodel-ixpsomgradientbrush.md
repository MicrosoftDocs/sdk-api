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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXpsOMGradientBrush
 - xpsobjectmodel/IXpsOMGradientBrush
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMGradientBrush
---

# IXpsOMGradientBrush interface

## -description

This interface describes a gradient that is made up of gradient stops. Classes that inherit from <b>IXpsOMGradientBrush</b> specify different ways of interpreting gradient stops.

<b>IXpsOMGradientBrush</b> is the base interface for the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomlineargradientbrush">IXpsOMLinearGradientBrush</a> and <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush">IXpsOMRadialGradientBrush</a> interfaces.

## -inheritance

The <b>IXpsOMGradientBrush</b> interface inherits from <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush">IXpsOMBrush</a>. <b>IXpsOMGradientBrush</b> also has these types of members:

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

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush">IXpsOMBrush</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomlineargradientbrush">IXpsOMLinearGradientBrush</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush">IXpsOMRadialGradientBrush</a>



<a href="/previous-versions/windows/desktop/dd316980(v=vs.85)">Interfaces</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>
