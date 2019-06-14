---
UID: NN:xpsobjectmodel.IXpsOMRadialGradientBrush
title: IXpsOMRadialGradientBrush (xpsobjectmodel.h)
author: windows-sdk-content
description: Specifies a radial gradient.
old-location: xps\ixpsomradialgradientbrush.htm
tech.root: printdocs
ms.assetid: 2f5b7b99-64a0-4156-8963-cfceb0d73503
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IXpsOMRadialGradientBrush, IXpsOMRadialGradientBrush interface [XPS Documents and Packaging], IXpsOMRadialGradientBrush interface [XPS Documents and Packaging],described, xps.ixpsomradialgradientbrush, xpsobjectmodel/IXpsOMRadialGradientBrush
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
 - IXpsOMRadialGradientBrush
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMRadialGradientBrush interface


## -description


Specifies a radial gradient.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMRadialGradientBrush</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush">IXpsOMGradientBrush</a>. <b>IXpsOMRadialGradientBrush</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMRadialGradientBrush</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomradialgradientbrush-clone">Clone</a>
</td>
<td align="left" width="63%">
Makes a deep copy of the interface. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomradialgradientbrush-getcenter">GetCenter</a>
</td>
<td align="left" width="63%">
Gets the center point of the radial gradient region ellipse.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomradialgradientbrush-getgradientorigin">GetGradientOrigin</a>
</td>
<td align="left" width="63%">
Gets the origin point of the radial gradient.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomradialgradientbrush-getradiisizes">GetRadiiSizes</a>
</td>
<td align="left" width="63%">
Gets the sizes of the radii that define the ellipse of the radial gradient region.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomradialgradientbrush-setcenter">SetCenter</a>
</td>
<td align="left" width="63%">
Sets the center point of the radial gradient region ellipse.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomradialgradientbrush-setgradientorigin">SetGradientOrigin</a>
</td>
<td align="left" width="63%">
Sets the origin point of the radial gradient.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomradialgradientbrush-setradiisizes">SetRadiiSizes</a>
</td>
<td align="left" width="63%">
Sets the sizes of the radii that define ellipse of the radial gradient region.

</td>
</tr>
</table> 


## -remarks



  As shown in the figure that follows, the gradient region of a radial gradient is the area enclosed by the ellipse that is described by the center point and the x and y radii that extend from the center point. The spread area is the area outside of that ellipse. The gradient path (not shown) is a radial line that is drawn between the gradient origin and the ellipse that bounds the gradient region.

<img alt="A figure that shows the terms used in a radial gradient" src="../images/RadialGradient1.png"/>
The code example that follows illustrates how to create an instance of  this interface.


```cpp

IXpsOMRadialGradientBrush    *newInterface;
// The following values are defined outside of 
// this example.
//  IXpsOMGradientStop       *gradStop1, *gradStop2;
//  XPS_POINT                centerPoint, gradientOrigin;
//  XPS_SIZE                 radiiSizes;

// Note the implicit requirement that CoInitializeEx 
//  has previously been called from this thread.

hr = CoCreateInstance(
    __uuidof(XpsOMObjectFactory),
    NULL,
    CLSCTX_INPROC_SERVER,
    _uuidof(IXpsOMObjectFactory),
    reinterpret_cast<LPVOID*>(&xpsFactory)
    );

if (SUCCEEDED(hr))
{
    hr = xpsFactory->CreateRadialGradientBrush (
        gradStop1,
        gradStop2,
        &centerPoint,
        &gradientOrigin,
        &radiiSizes,
        &newInterface);

    if (SUCCEEDED(hr))
    {
        // use newInterface

        newInterface->Release();
    }
    xpsFactory->Release();
}
else
{
    // evaluate HRESULT error returned in hr
}

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush">IXpsOMGradientBrush</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomlineargradientbrush">IXpsOMLinearGradientBrush</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createradialgradientbrush">IXpsOMObjectFactory::CreateRadialGradientBrush</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd316980(v=vs.85)">Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

