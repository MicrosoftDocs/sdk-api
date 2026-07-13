---
UID: NF:xpsobjectmodel.IXpsOMRadialGradientBrush.SetRadiiSizes
title: IXpsOMRadialGradientBrush::SetRadiiSizes (xpsobjectmodel.h)
description: Sets the sizes of the radii that define ellipse of the radial gradient region.
helpviewer_keywords: ["IXpsOMRadialGradientBrush interface [XPS Documents and Packaging]","SetRadiiSizes method","IXpsOMRadialGradientBrush.SetRadiiSizes","IXpsOMRadialGradientBrush::SetRadiiSizes","SetRadiiSizes","SetRadiiSizes method [XPS Documents and Packaging]","SetRadiiSizes method [XPS Documents and Packaging]","IXpsOMRadialGradientBrush interface","xps.ixpsomradialgradientbrush_setradiisizes","xpsobjectmodel/IXpsOMRadialGradientBrush::SetRadiiSizes"]
old-location: xps\ixpsomradialgradientbrush_setradiisizes.htm
tech.root: xps
ms.assetid: 2d32c0a7-1069-4c76-ba5c-5978e3fd7125
ms.date: 12/05/2018
ms.keywords: IXpsOMRadialGradientBrush interface [XPS Documents and Packaging],SetRadiiSizes method, IXpsOMRadialGradientBrush.SetRadiiSizes, IXpsOMRadialGradientBrush::SetRadiiSizes, SetRadiiSizes, SetRadiiSizes method [XPS Documents and Packaging], SetRadiiSizes method [XPS Documents and Packaging],IXpsOMRadialGradientBrush interface, xps.ixpsomradialgradientbrush_setradiisizes, xpsobjectmodel/IXpsOMRadialGradientBrush::SetRadiiSizes
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
 - IXpsOMRadialGradientBrush::SetRadiiSizes
 - xpsobjectmodel/IXpsOMRadialGradientBrush::SetRadiiSizes
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
 - IXpsOMRadialGradientBrush.SetRadiiSizes
---

# IXpsOMRadialGradientBrush::SetRadiiSizes


## -description

Sets the sizes of the radii that define ellipse of the radial gradient region.

## -parameters

### -param radiiSizes [in]

The <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_size">XPS_SIZE</a> structure that  receives the sizes of the radii.

<table>
<tr>
<th>Field</th>
<th>Meaning</th>
</tr>
<tr>
<td>
<b>width</b>

</td>
<td>
Size of the radius along the x-axis.

</td>
</tr>
<tr>
<td>
<b>height</b>

</td>
<td>
Size of the radius along the y-axis.

</td>
</tr>
</table>
 

Size is described in XPS units. There are 96 XPS units per inch. For example, a 1" radius is 96 XPS units.

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
One of the sizes described by <i>radiiSizes</i> is not valid. The <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_size">XPS_SIZE</a> structure must contain valid, finite, and non-negative floating-point values.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>radiiSizes</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The following illustration identifies the parts of a radial gradient.    <i>radiiSizes.width</i> sets the x-radius,  and <i>radiiSizes.height</i> the y-radius. For a more detailed description of this diagram, see <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush">IXpsOMRadialGradientBrush</a>.

<img alt="A figure that shows the terms used in a radial gradient" src="./images/RadialGradient1.png"/>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush">IXpsOMRadialGradientBrush</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>



<a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_size">XPS_SIZE</a>