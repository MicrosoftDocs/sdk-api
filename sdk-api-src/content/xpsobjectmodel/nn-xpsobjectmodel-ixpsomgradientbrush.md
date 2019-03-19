---
UID: NN:xpsobjectmodel.IXpsOMGradientBrush
title: IXpsOMGradientBrush (xpsobjectmodel.h)
author: windows-sdk-content
description: This interface describes a gradient that is made up of gradient stops. Classes that inherit from IXpsOMGradientBrush specify different ways of interpreting gradient stops.
old-location: xps\ixpsomgradientbrush.htm
tech.root: printdocs
ms.assetid: d381b813-5368-4ffe-a9a1-0f5027ae9d80
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IXpsOMGradientBrush, IXpsOMGradientBrush interface [XPS Documents and Packaging], IXpsOMGradientBrush interface [XPS Documents and Packaging],described, xps.ixpsomgradientbrush, xpsobjectmodel/IXpsOMGradientBrush
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMGradientBrush interface


## -description


This interface describes a gradient that is made up of gradient stops. Classes that inherit from <b>IXpsOMGradientBrush</b> specify different ways of interpreting gradient stops.

<b>IXpsOMGradientBrush</b> is the base interface for the <a href="https://msdn.microsoft.com/739bf088-0f09-47c1-9b49-6c279395f15b">IXpsOMLinearGradientBrush</a> and <a href="https://msdn.microsoft.com/2f5b7b99-64a0-4156-8963-cfceb0d73503">IXpsOMRadialGradientBrush</a> interfaces.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMGradientBrush</b> interface inherits from <a href="https://msdn.microsoft.com/43cb56db-e09e-47cb-b50b-7827131659fd">IXpsOMBrush</a>. <b>IXpsOMGradientBrush</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/4e58c019-d89d-472d-9b6f-b335b184f998">GetColorInterpolationMode</a>
</td>
<td align="left" width="63%">
Gets the gamma function to be used for color interpolation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1b308323-12d4-427c-a3d8-fcf5488e1dde">GetGradientStops</a>
</td>
<td align="left" width="63%">
Gets a pointer to an <a href="https://msdn.microsoft.com/1f51f818-e9bb-4d88-9795-4e6890d24b8c">IXpsOMGradientStopCollection</a> interface that contains the collection of <a href="https://msdn.microsoft.com/e115d806-70c1-4c6a-810e-e6a058628b44">IXpsOMGradientStop</a> interfaces that define the gradient.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c4c62817-735b-4ef1-84cf-1c9fa63f55ee">GetSpreadMethod</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/en-us/library/Dd372989(v=VS.85).aspx">XPS_SPREAD_METHOD</a> value, which describes how the area outside of the gradient region will be rendered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b5474d2-a97e-4446-b4a9-7efb51c31ad3">GetTransform</a>
</td>
<td align="left" width="63%">
Gets a pointer to the <a href="https://msdn.microsoft.com/d21457bc-9445-4ca2-ab9f-1e3f55e2e635">IXpsOMMatrixTransform</a> interface that contains the resolved matrix transform for the brush.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dfdd6797-b7e6-46fa-92b1-d9c418e8a510">GetTransformLocal</a>
</td>
<td align="left" width="63%">
Gets a pointer to the <a href="https://msdn.microsoft.com/d21457bc-9445-4ca2-ab9f-1e3f55e2e635">IXpsOMMatrixTransform</a> interface that contains the local, unshared, resolved matrix transform for the brush.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/60a91156-f9c8-4f6b-92b7-21e2fcd337fc">GetTransformLookup</a>
</td>
<td align="left" width="63%">
Gets the name of the lookup key  of the shared matrix transform interface that is to be used for the brush.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f9fa44e7-336a-4758-ac53-b2d527336b7d">SetColorInterpolationMode</a>
</td>
<td align="left" width="63%">
Sets the <a href="https://msdn.microsoft.com/en-us/library/Dd372940(v=VS.85).aspx">XPS_COLOR_INTERPOLATION</a> value, which describes the gamma function to be used for color interpolation.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2114ba2e-95df-466e-983f-a56491bf891c">SetSpreadMethod</a>
</td>
<td align="left" width="63%">
Sets the <a href="https://msdn.microsoft.com/en-us/library/Dd372989(v=VS.85).aspx">XPS_SPREAD_METHOD</a> value, which describes how the area outside of the gradient region is to be rendered.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aabb0410-bdff-4b6b-8d8a-de1cc6fca68b">SetTransformLocal</a>
</td>
<td align="left" width="63%">
Sets the <a href="https://msdn.microsoft.com/d21457bc-9445-4ca2-ab9f-1e3f55e2e635">IXpsOMMatrixTransform</a> interface pointer to a local, unshared matrix transform that is to be used for the brush.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/342434ff-9fdc-43ea-8beb-9d518f7a9454">SetTransformLookup</a>
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

<img alt="A figure that shows the terms used in a linear gradient" src="../images/LinearGradient1.png"/>
As shown in the figure that follows, the gradient region of a radial gradient is the area enclosed by the ellipse that is described by the center point and the x and y radii that extend from the center point. The spread area is the area outside of that ellipse. The gradient path is a radial line that sweeps the entire gradient region from the gradient origin to the ellipse that bounds the gradient region. In the following illustration, the gradient path is not shown.

<img alt="A figure that shows the terms used in a radial gradient" src="../images/RadialGradient1.png"/>
The spread method describes how the spread area is filled. Implementation of the spread method depends on the gradient type (linear or radial). The following illustration shows several examples of how the spread area can be filled. For  information about different spread methods, see <a href="https://msdn.microsoft.com/en-us/library/Dd372989(v=VS.85).aspx">XPS_SPREAD_METHOD</a>.

<img alt="An illustration that shows examples of the spread method" src="../images/XPS_Spread_Method.png"/>
 The transform  determines how the resulting gradient is transformed. The visible part of the gradient that is ultimately rendered in the image is determined by the path, stroke, or glyph that is using the gradient brush.




## -see-also




<a href="https://msdn.microsoft.com/43cb56db-e09e-47cb-b50b-7827131659fd">IXpsOMBrush</a>



<a href="https://msdn.microsoft.com/739bf088-0f09-47c1-9b49-6c279395f15b">IXpsOMLinearGradientBrush</a>



<a href="https://msdn.microsoft.com/2f5b7b99-64a0-4156-8963-cfceb0d73503">IXpsOMRadialGradientBrush</a>



<a href="https://msdn.microsoft.com/8d72ff28-6dfb-4fa8-a1b6-14b054aa7eb5">Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

