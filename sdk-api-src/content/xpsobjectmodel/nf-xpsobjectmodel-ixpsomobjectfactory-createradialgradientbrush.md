---
UID: NF:xpsobjectmodel.IXpsOMObjectFactory.CreateRadialGradientBrush
title: IXpsOMObjectFactory::CreateRadialGradientBrush (xpsobjectmodel.h)
description: Creates an IXpsOMRadialGradientBrush interface.
helpviewer_keywords: ["CreateRadialGradientBrush","CreateRadialGradientBrush method [XPS Documents and Packaging]","CreateRadialGradientBrush method [XPS Documents and Packaging]","IXpsOMObjectFactory interface","IXpsOMObjectFactory interface [XPS Documents and Packaging]","CreateRadialGradientBrush method","IXpsOMObjectFactory.CreateRadialGradientBrush","IXpsOMObjectFactory::CreateRadialGradientBrush","xps.ixpsomobjectfactory_createradialgradientbrush","xpsobjectmodel/IXpsOMObjectFactory::CreateRadialGradientBrush"]
old-location: xps\ixpsomobjectfactory_createradialgradientbrush.htm
tech.root: xps
ms.assetid: b91c9490-1995-48cb-a313-ef83f00b9c50
ms.date: 12/05/2018
ms.keywords: CreateRadialGradientBrush, CreateRadialGradientBrush method [XPS Documents and Packaging], CreateRadialGradientBrush method [XPS Documents and Packaging],IXpsOMObjectFactory interface, IXpsOMObjectFactory interface [XPS Documents and Packaging],CreateRadialGradientBrush method, IXpsOMObjectFactory.CreateRadialGradientBrush, IXpsOMObjectFactory::CreateRadialGradientBrush, xps.ixpsomobjectfactory_createradialgradientbrush, xpsobjectmodel/IXpsOMObjectFactory::CreateRadialGradientBrush
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
 - IXpsOMObjectFactory::CreateRadialGradientBrush
 - xpsobjectmodel/IXpsOMObjectFactory::CreateRadialGradientBrush
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
 - IXpsOMObjectFactory.CreateRadialGradientBrush
---

# IXpsOMObjectFactory::CreateRadialGradientBrush


## -description

Creates an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush">IXpsOMRadialGradientBrush</a> interface.

## -parameters

### -param gradStop1 [in]

The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstop">IXpsOMGradientStop</a> interface that specifies the  properties of the gradient  at gradient origin. This parameter must not be <b>NULL</b>.

### -param gradStop2 [in]

The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstop">IXpsOMGradientStop</a> interface that specifies the  properties of the gradient  at the end of  the gradient's vector, which is the ellipse that encloses the gradient region. This parameter must not be <b>NULL</b>.

### -param centerPoint [in]

The coordinates of the center point of the radial gradient ellipse.

### -param gradientOrigin [in]

The coordinates of the origin  of the radial gradient.

### -param radiiSizes [in]

The <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_size">XPS_SIZE</a> structure whose members specify the lengths of the gradient region's radii.

Size is described in XPS units. There are 96 XPS units per inch. For example, a 1" radius is 96 XPS units.

<table>
<tr>
<th>
<a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_size">XPS_SIZE</a> Member</th>
<th>Meaning</th>
</tr>
<tr>
<td>
<b>width</b>

</td>
<td>
Length of the radius  along the x-axis.

</td>
</tr>
<tr>
<td>
<b>height</b>

</td>
<td>
Length of the radius  along the y-axis.

</td>
</tr>
</table>

### -param radialGradientBrush [out, retval]

A pointer to the new <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush">IXpsOMRadialGradientBrush</a> interface.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The point that is described by <i>centerPoint</i>, <i>radiiSizes</i>, or <i>gradientOrigin</i> is not valid. The members of the <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_point">XPS_POINT</a> structure must contain valid and finite floating-point values.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>gradStop1</i>,  <i>gradStop2</i>, <i>centerPoint</i>, <i>gradientOrigin</i>, <i>radiiSizes</i>, or <i>radialGradientBrush</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_NO_CUSTOM_OBJECTS</b></dt>
</dl>
</td>
<td width="60%">
<i>gradStop1</i>  or <i>gradStop1</i> does not point to a recognized interface implementation. Custom implementation of XPS Document API interfaces is not supported.

</td>
</tr>
</table>

## -remarks

  As shown in the following illustration, the gradient region of a radial gradient is the area enclosed by the ellipse that is described by the center point and the x and y radii that extend from the center point. The spread area is the area outside of that ellipse. The gradient path (not shown) is a radial line that is drawn between the gradient origin and the ellipse that bounds the gradient region.

<img alt="A figure that shows the terms used in a radial gradient" src="./images/RadialGradient1.png"/>
For radial-gradient brushes, the gradient stop that is set by the <i>gradStop1</i> parameter corresponds to the gradient origin location and an offset value of 0.0. The gradient stop that is set by the <i>gradStop2</i> parameter corresponds to the circumference of the gradient region and an offset value of 1.0. For more information on gradient stops, see <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstop">IXpsOMGradientStop</a>.

The code example that follows illustrates how this method is used to create a new  interface.


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

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstop">IXpsOMGradientStop</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory">IXpsOMObjectFactory</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush">IXpsOMRadialGradientBrush</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>



<a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_point">XPS_POINT</a>



<a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_size">XPS_SIZE</a>