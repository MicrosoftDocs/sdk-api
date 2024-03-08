---
UID: NN:xpsobjectmodel.IXpsOMGradientStop
title: IXpsOMGradientStop (xpsobjectmodel.h)
description: Represents a single color and location within a gradient.
helpviewer_keywords: ["IXpsOMGradientStop","IXpsOMGradientStop interface [XPS Documents and Packaging]","IXpsOMGradientStop interface [XPS Documents and Packaging]","described","xps.ixpsomgradientstop","xpsobjectmodel/IXpsOMGradientStop"]
old-location: xps\ixpsomgradientstop.htm
tech.root: xps
ms.assetid: e115d806-70c1-4c6a-810e-e6a058628b44
ms.date: 12/05/2018
ms.keywords: IXpsOMGradientStop, IXpsOMGradientStop interface [XPS Documents and Packaging], IXpsOMGradientStop interface [XPS Documents and Packaging],described, xps.ixpsomgradientstop, xpsobjectmodel/IXpsOMGradientStop
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
 - IXpsOMGradientStop
 - xpsobjectmodel/IXpsOMGradientStop
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
 - IXpsOMGradientStop
---

# IXpsOMGradientStop interface

## -description

Represents a single color and location within a gradient.

## -inheritance

The <b>IXpsOMGradientStop</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IXpsOMGradientStop</b> also has these types of members:

## -remarks

A gradient stop is a specific color that  is defined for a location within the gradient region. The color of the gradient changes between the gradient stops of the gradient. The area and absolute location of the gradient is defined by the gradient interface.   The offset is a relative location within the gradient region and is measured between 0.0 and 1.0. An offset of  0.0 is the beginning of the gradient and 1.0 is the end. Gradient stops can be defined for any offset within the range, including the end points. This interface describes one and only one stop in a gradient.

The gradient path is the straight line that connects the start point and the end point of a linear gradient. The gradient region of a linear gradient consists of the area between the start point and the end point, including those points, and extends in both directions at a right angle to the gradient path. The spread area is the area outside the gradient region. 

Gradient stops  define the color at a specific location along the gradient path; the color is interpolated along the gradient path between the gradient stops. In the example that follows, the gradient region fills the image, so there is no spread area.

For gradient stops used in linear-gradient brushes, the offset value of 0.0 corresponds to the start point of the gradient path, and the offset value of 1.0 corresponds to the end point. To determine the location of a gradient stop between these two points, intermediate offset values are interpolated between them. The following illustration shows two intermediate gradient stops, one at an offset of 0.25 and another at 0.75.

<img alt="A figure that shows the terms used in a linear gradient" src="./images/LinearGradient2.png"/>


For gradient stops used in radial-gradient brushes, the offset value of 0.0 corresponds to the gradient origin location, and the offset value of 1.0 corresponds to the circumference of the ellipse that bounds the gradient. Offsets between 0.0 and 1.0 define an ellipse that is interpolated between the gradient origin  and the bounding ellipse. The illustration  that follows has one intermediate gradient stop at an offset of 0.50 (Gradient stop 1). The gradient  is using the <b>XPS_SPREAD_METHOD_REFLECT</b> spread method to fill the space outside of the gradient region.

<img alt="A figure that shows the terms used in a radial gradient" src="./images/RadialGradient2.png"/>
The calculations that are used to render a gradient are  described  in the <a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>.

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

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush">IXpsOMGradientBrush</a>



<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-creategradientstop">IXpsOMObjectFactory::CreateGradientStop</a>



<a href="/previous-versions/windows/desktop/dd316980(v=vs.85)">Interfaces</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>
