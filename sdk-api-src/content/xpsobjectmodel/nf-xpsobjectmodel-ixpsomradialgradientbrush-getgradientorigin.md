---
UID: NF:xpsobjectmodel.IXpsOMRadialGradientBrush.GetGradientOrigin
title: IXpsOMRadialGradientBrush::GetGradientOrigin (xpsobjectmodel.h)
description: Gets the origin point of the radial gradient.
helpviewer_keywords: ["GetGradientOrigin","GetGradientOrigin method [XPS Documents and Packaging]","GetGradientOrigin method [XPS Documents and Packaging]","IXpsOMRadialGradientBrush interface","IXpsOMRadialGradientBrush interface [XPS Documents and Packaging]","GetGradientOrigin method","IXpsOMRadialGradientBrush.GetGradientOrigin","IXpsOMRadialGradientBrush::GetGradientOrigin","xps.ixpsomradialgradientbrush_getgradientorigin","xpsobjectmodel/IXpsOMRadialGradientBrush::GetGradientOrigin"]
old-location: xps\ixpsomradialgradientbrush_getgradientorigin.htm
tech.root: xps
ms.assetid: 44e55c42-a18b-45dd-aa92-b9336eedd9ad
ms.date: 12/05/2018
ms.keywords: GetGradientOrigin, GetGradientOrigin method [XPS Documents and Packaging], GetGradientOrigin method [XPS Documents and Packaging],IXpsOMRadialGradientBrush interface, IXpsOMRadialGradientBrush interface [XPS Documents and Packaging],GetGradientOrigin method, IXpsOMRadialGradientBrush.GetGradientOrigin, IXpsOMRadialGradientBrush::GetGradientOrigin, xps.ixpsomradialgradientbrush_getgradientorigin, xpsobjectmodel/IXpsOMRadialGradientBrush::GetGradientOrigin
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
 - IXpsOMRadialGradientBrush::GetGradientOrigin
 - xpsobjectmodel/IXpsOMRadialGradientBrush::GetGradientOrigin
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
 - IXpsOMRadialGradientBrush.GetGradientOrigin
---

# IXpsOMRadialGradientBrush::GetGradientOrigin


## -description

Gets the origin point of the radial gradient.

## -parameters

### -param origin [out, retval]

The x and y coordinates of the radial gradient's origin point.

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
<i>origin</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The x and y coordinates that are specified in <i>origin</i>   are relative to the page and are expressed in units of the  transform  that is in effect.

The following illustration shows the parts of a radial gradient. <i>origin</i> gets the location of the gradient origin.   For a more detailed description of this diagram, see <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush">IXpsOMRadialGradientBrush</a>.

<img alt="A figure that shows the terms used in a radial gradient" src="./images/RadialGradient1.png"/>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush">IXpsOMRadialGradientBrush</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>



<a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_point">XPS_POINT</a>