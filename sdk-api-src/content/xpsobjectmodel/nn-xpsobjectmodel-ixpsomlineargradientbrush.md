---
UID: NN:xpsobjectmodel.IXpsOMLinearGradientBrush
title: IXpsOMLinearGradientBrush (xpsobjectmodel.h)
description: Specifies a linear gradient, which is the color gradient along a vector.
helpviewer_keywords: ["IXpsOMLinearGradientBrush","IXpsOMLinearGradientBrush interface [XPS Documents and Packaging]","IXpsOMLinearGradientBrush interface [XPS Documents and Packaging]","described","xps.ixpsomlineargradientbrush","xpsobjectmodel/IXpsOMLinearGradientBrush"]
old-location: xps\ixpsomlineargradientbrush.htm
tech.root: xps
ms.assetid: 739bf088-0f09-47c1-9b49-6c279395f15b
ms.date: 12/05/2018
ms.keywords: IXpsOMLinearGradientBrush, IXpsOMLinearGradientBrush interface [XPS Documents and Packaging], IXpsOMLinearGradientBrush interface [XPS Documents and Packaging],described, xps.ixpsomlineargradientbrush, xpsobjectmodel/IXpsOMLinearGradientBrush
f1_keywords:
- xpsobjectmodel/IXpsOMLinearGradientBrush
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
- IXpsOMLinearGradientBrush
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMLinearGradientBrush interface


## -description


Specifies a linear gradient, which is the color gradient along a vector.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMLinearGradientBrush</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush">IXpsOMGradientBrush</a>. <b>IXpsOMLinearGradientBrush</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMLinearGradientBrush</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomlineargradientbrush-clone">Clone</a>
</td>
<td align="left" width="63%">
Makes a deep copy of the interface. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomlineargradientbrush-getendpoint">GetEndPoint</a>
</td>
<td align="left" width="63%">
Gets the end point of the gradient.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomlineargradientbrush-getstartpoint">GetStartPoint</a>
</td>
<td align="left" width="63%">
Gets the start point of the gradient.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomlineargradientbrush-setendpoint">SetEndPoint</a>
</td>
<td align="left" width="63%">
Sets the end point of the gradient.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomlineargradientbrush-setstartpoint">SetStartPoint</a>
</td>
<td align="left" width="63%">
Sets the start point of the gradient.

</td>
</tr>
</table> 


## -remarks



In the illustration that follows, the start and end points of a linear gradient are also the start and end points of the gradient path, which is the straight line that connects those points.

The gradient region of a linear gradient is the area between and including the start and end points and extending in both directions at a right angle to the gradient path. The spread area is the area of the geometry that lies outside the gradient region.

Gradient stops are used to define the color at specific locations along the gradient path. In the illustration, gradient stop 0 is located at the start point of the gradient path, and gradient stop 1 is at the end point. The <b>XPS_SPREAD_METHOD_PAD</b> spread method is used to fill the spread area.

<img alt="A figure that shows the terms used in a linear gradient" src="./images/LinearGradient1.png"/>
The code example that follows illustrates how to create an instance of  this interface.


```cpp

IXpsOMLinearGradientBrush    *newInterface;
// The following values are defined outside of 
// this example.
//  IXpsOMGradientStop       *gradStop1, *gradStop2;
//  XPS_POINT                startPoint, endPoint;

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
    hr = xpsFactory->CreateLinearGradientBrush (
        gradStop1,
        gradStop2,
        &startPoint,
        &endPoint,
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



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstop">IXpsOMGradientStop</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createlineargradientbrush">IXpsOMObjectFactory::CreateLinearGradientBrush</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush">IXpsOMRadialGradientBrush</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd316980(v=vs.85)">Interfaces</a>



<a href="https://www.microsoft.com/download/details.aspx?id=11816">XML Paper Specification</a>
 

 

