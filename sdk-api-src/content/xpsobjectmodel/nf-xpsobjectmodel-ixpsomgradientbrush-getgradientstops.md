---
UID: NF:xpsobjectmodel.IXpsOMGradientBrush.GetGradientStops
title: IXpsOMGradientBrush::GetGradientStops (xpsobjectmodel.h)
description: Gets a pointer to an IXpsOMGradientStopCollection interface that contains the collection of IXpsOMGradientStop interfaces that define the gradient.
helpviewer_keywords: ["GetGradientStops","GetGradientStops method [XPS Documents and Packaging]","GetGradientStops method [XPS Documents and Packaging]","IXpsOMGradientBrush interface","IXpsOMGradientBrush interface [XPS Documents and Packaging]","GetGradientStops method","IXpsOMGradientBrush.GetGradientStops","IXpsOMGradientBrush::GetGradientStops","xps.ixpsomgradientbrush_getgradientstops","xpsobjectmodel/IXpsOMGradientBrush::GetGradientStops"]
old-location: xps\ixpsomgradientbrush_getgradientstops.htm
tech.root: xps
ms.assetid: 1b308323-12d4-427c-a3d8-fcf5488e1dde
ms.date: 12/05/2018
ms.keywords: GetGradientStops, GetGradientStops method [XPS Documents and Packaging], GetGradientStops method [XPS Documents and Packaging],IXpsOMGradientBrush interface, IXpsOMGradientBrush interface [XPS Documents and Packaging],GetGradientStops method, IXpsOMGradientBrush.GetGradientStops, IXpsOMGradientBrush::GetGradientStops, xps.ixpsomgradientbrush_getgradientstops, xpsobjectmodel/IXpsOMGradientBrush::GetGradientStops
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
 - IXpsOMGradientBrush::GetGradientStops
 - xpsobjectmodel/IXpsOMGradientBrush::GetGradientStops
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
 - IXpsOMGradientBrush.GetGradientStops
---

# IXpsOMGradientBrush::GetGradientStops


## -description

Gets a pointer to an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstopcollection">IXpsOMGradientStopCollection</a> interface that contains the collection of <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstop">IXpsOMGradientStop</a> interfaces that define the gradient.

## -parameters

### -param gradientStops [out, retval]

A pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstopcollection">IXpsOMGradientStopCollection</a> interface that contains the collection of <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstop">IXpsOMGradientStop</a> interfaces.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>gradientStops</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

Gradient stops, which are  described  in the XPS OM by an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstop">IXpsOMGradientStop</a> interface, are used to define the color at a specific location along a gradient path; the color is interpolated between the gradient stops. The illustration that follows shows the gradient path and gradient stops of a linear gradient.

<img alt="A figure that shows the terms used in a linear gradient" src="./images/LinearGradient2.png"/>
The illustration that follows shows the gradient stops of a radial gradient. In this example, the gradient region is the area enclosed by the outer ellipse, and the radial gradient is using the <b>XPS_SPREAD_METHOD_REFLECT</b> spread method to fill the space outside of the gradient region.

<img alt="A figure that shows the terms used in a radial gradient" src="./images/RadialGradient2.png"/>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush">IXpsOMGradientBrush</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstop">IXpsOMGradientStop</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>