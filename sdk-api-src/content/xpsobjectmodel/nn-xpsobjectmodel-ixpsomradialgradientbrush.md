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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMRadialGradientBrush</b> interface inherits from <a href="https://msdn.microsoft.com/d381b813-5368-4ffe-a9a1-0f5027ae9d80">IXpsOMGradientBrush</a>. <b>IXpsOMRadialGradientBrush</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/be715ef5-9d75-464d-ab72-da2a4047d1e5">Clone</a>
</td>
<td align="left" width="63%">
Makes a deep copy of the interface. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/92ce3433-6c3d-4759-81f8-055fdcc58dcf">GetCenter</a>
</td>
<td align="left" width="63%">
Gets the center point of the radial gradient region ellipse.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/44e55c42-a18b-45dd-aa92-b9336eedd9ad">GetGradientOrigin</a>
</td>
<td align="left" width="63%">
Gets the origin point of the radial gradient.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c57c125b-7a21-4b94-b4c3-1aa34d615a12">GetRadiiSizes</a>
</td>
<td align="left" width="63%">
Gets the sizes of the radii that define the ellipse of the radial gradient region.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f1fd304-8495-40b3-b11f-7af9924150eb">SetCenter</a>
</td>
<td align="left" width="63%">
Sets the center point of the radial gradient region ellipse.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/101bebbf-854c-49fa-bc5c-8c81c5d2f7f9">SetGradientOrigin</a>
</td>
<td align="left" width="63%">
Sets the origin point of the radial gradient.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2d32c0a7-1069-4c76-ba5c-5978e3fd7125">SetRadiiSizes</a>
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




<a href="https://msdn.microsoft.com/d381b813-5368-4ffe-a9a1-0f5027ae9d80">IXpsOMGradientBrush</a>



<a href="https://msdn.microsoft.com/739bf088-0f09-47c1-9b49-6c279395f15b">IXpsOMLinearGradientBrush</a>



<a href="https://msdn.microsoft.com/b91c9490-1995-48cb-a313-ef83f00b9c50">IXpsOMObjectFactory::CreateRadialGradientBrush</a>



<a href="https://msdn.microsoft.com/8d72ff28-6dfb-4fa8-a1b6-14b054aa7eb5">Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

