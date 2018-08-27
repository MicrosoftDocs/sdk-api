---
UID: NN:xpsobjectmodel.IXpsOMLinearGradientBrush
title: IXpsOMLinearGradientBrush
author: windows-sdk-content
description: Specifies a linear gradient, which is the color gradient along a vector.
old-location: xps\ixpsomlineargradientbrush.htm
old-project: printdocs
ms.assetid: 739bf088-0f09-47c1-9b49-6c279395f15b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IXpsOMLinearGradientBrush, IXpsOMLinearGradientBrush interface [XPS Documents and Packaging], IXpsOMLinearGradientBrush interface [XPS Documents and Packaging],described, xps.ixpsomlineargradientbrush, xpsobjectmodel/IXpsOMLinearGradientBrush
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: xpsobjectmodel.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: XPS_INTERLEAVING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMLinearGradientBrush
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMLinearGradientBrush interface


## -description


Specifies a linear gradient, which is the color gradient along a vector.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMLinearGradientBrush</b> interface inherits from <a href="https://msdn.microsoft.com/d381b813-5368-4ffe-a9a1-0f5027ae9d80">IXpsOMGradientBrush</a>. <b>IXpsOMLinearGradientBrush</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/b0c44a37-e7fb-4079-a299-cb09635f61ca">Clone</a>
</td>
<td align="left" width="63%">
Makes a deep copy of the interface. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c8f34c4b-28f1-4a8f-bf8e-9872debc9eb1">GetEndPoint</a>
</td>
<td align="left" width="63%">
Gets the end point of the gradient.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/03e9884b-6249-4ccb-a6ee-d360655c5f75">GetStartPoint</a>
</td>
<td align="left" width="63%">
Gets the start point of the gradient.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5eec7bda-bbd8-454a-8b32-9db769df91e6">SetEndPoint</a>
</td>
<td align="left" width="63%">
Sets the end point of the gradient.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f2e40d75-c0de-4cba-850d-0c8c328e2950">SetStartPoint</a>
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

<img alt="A figure that shows the terms used in a linear gradient" src="../images/LinearGradient1.png"/>
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




<a href="https://msdn.microsoft.com/d381b813-5368-4ffe-a9a1-0f5027ae9d80">IXpsOMGradientBrush</a>



<a href="https://msdn.microsoft.com/e115d806-70c1-4c6a-810e-e6a058628b44">IXpsOMGradientStop</a>



<a href="https://msdn.microsoft.com/b829e8fe-5ef0-43d8-b115-9cddbfe1a255">IXpsOMObjectFactory::CreateLinearGradientBrush</a>



<a href="https://msdn.microsoft.com/2f5b7b99-64a0-4156-8963-cfceb0d73503">IXpsOMRadialGradientBrush</a>



<a href="https://msdn.microsoft.com/8d72ff28-6dfb-4fa8-a1b6-14b054aa7eb5">Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

