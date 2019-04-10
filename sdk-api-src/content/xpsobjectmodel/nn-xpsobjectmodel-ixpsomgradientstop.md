---
UID: NN:xpsobjectmodel.IXpsOMGradientStop
title: IXpsOMGradientStop (xpsobjectmodel.h)
author: windows-sdk-content
description: Represents a single color and location within a gradient.
old-location: xps\ixpsomgradientstop.htm
tech.root: printdocs
ms.assetid: e115d806-70c1-4c6a-810e-e6a058628b44
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IXpsOMGradientStop, IXpsOMGradientStop interface [XPS Documents and Packaging], IXpsOMGradientStop interface [XPS Documents and Packaging],described, xps.ixpsomgradientstop, xpsobjectmodel/IXpsOMGradientStop
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
 - IXpsOMGradientStop
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMGradientStop interface


## -description


Represents a single color and location within a gradient.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMGradientStop</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IXpsOMGradientStop</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMGradientStop</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ea4cdf1d-bb65-4a1b-b5bc-3eb1e90929ff">Clone</a>
</td>
<td align="left" width="63%">
Makes a deep copy of the <b>IXpsOMGradientStop</b> interface.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6630d58f-d0f0-4b39-a14c-d3955f0f401a">GetColor</a>
</td>
<td align="left" width="63%">
Gets the color value and color profile of the gradient stop.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/14048707-1a73-40a1-9094-da4885d9934d">GetOffset</a>
</td>
<td align="left" width="63%">
Gets the offset value of the gradient stop.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a590e461-bf86-4379-b29a-ecdba57bd3f8">GetOwner</a>
</td>
<td align="left" width="63%">
Gets a pointer to the <a href="https://msdn.microsoft.com/d381b813-5368-4ffe-a9a1-0f5027ae9d80">IXpsOMGradientBrush</a> interface that contains the gradient stop.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/535b14f3-6d17-4c3c-b310-b018922d48e8">SetColor</a>
</td>
<td align="left" width="63%">
Sets the color value and color profile of the gradient stop.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c1932b0-386b-4779-a4e4-e239e42e1d16">SetOffset</a>
</td>
<td align="left" width="63%">
Sets the offset location of the gradient stop.

</td>
</tr>
</table> 


## -remarks



A gradient stop is a specific color that  is defined for a location within the gradient region. The color of the gradient changes between the gradient stops of the gradient. The area and absolute location of the gradient is defined by the gradient interface.   The offset is a relative location within the gradient region and is measured between 0.0 and 1.0. An offset of  0.0 is the beginning of the gradient and 1.0 is the end. Gradient stops can be defined for any offset within the range, including the end points. This interface describes one and only one stop in a gradient.

The gradient path is the straight line that connects the start point and the end point of a linear gradient. The gradient region of a linear gradient consists of the area between the start point and the end point, including those points, and extends in both directions at a right angle to the gradient path. The spread area is the area outside the gradient region. 

Gradient stops  define the color at a specific location along the gradient path; the color is interpolated along the gradient path between the gradient stops. In the example that follows, the gradient region fills the image, so there is no spread area.

For gradient stops used in linear-gradient brushes, the offset value of 0.0 corresponds to the start point of the gradient path, and the offset value of 1.0 corresponds to the end point. To determine the location of a gradient stop between these two points, intermediate offset values are interpolated between them. The following illustration shows two intermediate gradient stops, one at an offset of 0.25 and another at 0.75.

<img alt="A figure that shows the terms used in a linear gradient" src="../images/LinearGradient2.png"/>


For gradient stops used in radial-gradient brushes, the offset value of 0.0 corresponds to the gradient origin location, and the offset value of 1.0 corresponds to the circumference of the ellipse that bounds the gradient. Offsets between 0.0 and 1.0 define an ellipse that is interpolated between the gradient origin  and the bounding ellipse. The illustration  that follows has one intermediate gradient stop at an offset of 0.50 (Gradient stop 1). The gradient  is using the <b>XPS_SPREAD_METHOD_REFLECT</b> spread method to fill the space outside of the gradient region.

<img alt="A figure that shows the terms used in a radial gradient" src="../images/RadialGradient2.png"/>
The calculations that are used to render a gradient are  described  in the <a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>.

The code example that follows illustrates how to create an instance of  this interface.


```cpp

IXpsOMGradientStop    *newInterface;
// The following values are defined outside of 
// this example.
//  XPS_COLOR                    color;
//  IXpsOMColorProfileResource    *colorProfile;
//  FLOAT                        offset;

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
    hr = xpsFactory->CreateGradientStop (
        &color,
        colorProfile,
        offset,
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



<a href="https://msdn.microsoft.com/c9217444-fc9d-4b1e-abb2-7e1badd32052">IXpsOMObjectFactory::CreateGradientStop</a>



<a href="https://msdn.microsoft.com/8d72ff28-6dfb-4fa8-a1b6-14b054aa7eb5">Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

