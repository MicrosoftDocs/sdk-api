---
UID: NF:xpsobjectmodel.IXpsOMLinearGradientBrush.SetEndPoint
title: IXpsOMLinearGradientBrush::SetEndPoint (xpsobjectmodel.h)
description: Sets the end point of the gradient.
helpviewer_keywords: ["IXpsOMLinearGradientBrush interface [XPS Documents and Packaging]","SetEndPoint method","IXpsOMLinearGradientBrush.SetEndPoint","IXpsOMLinearGradientBrush::SetEndPoint","SetEndPoint","SetEndPoint method [XPS Documents and Packaging]","SetEndPoint method [XPS Documents and Packaging]","IXpsOMLinearGradientBrush interface","xps.ixpsomlineargradientbrush_setendpoint","xpsobjectmodel/IXpsOMLinearGradientBrush::SetEndPoint"]
old-location: xps\ixpsomlineargradientbrush_setendpoint.htm
tech.root: xps
ms.assetid: 5eec7bda-bbd8-454a-8b32-9db769df91e6
ms.date: 12/05/2018
ms.keywords: IXpsOMLinearGradientBrush interface [XPS Documents and Packaging],SetEndPoint method, IXpsOMLinearGradientBrush.SetEndPoint, IXpsOMLinearGradientBrush::SetEndPoint, SetEndPoint, SetEndPoint method [XPS Documents and Packaging], SetEndPoint method [XPS Documents and Packaging],IXpsOMLinearGradientBrush interface, xps.ixpsomlineargradientbrush_setendpoint, xpsobjectmodel/IXpsOMLinearGradientBrush::SetEndPoint
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
 - IXpsOMLinearGradientBrush::SetEndPoint
 - xpsobjectmodel/IXpsOMLinearGradientBrush::SetEndPoint
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
 - IXpsOMLinearGradientBrush.SetEndPoint
---

# IXpsOMLinearGradientBrush::SetEndPoint


## -description

Sets the end point of the gradient.

## -parameters

### -param endPoint [in]

The x and y coordinates of the end point.

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
The point described by <i>endPoint</i> was not valid. The <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_point">XPS_POINT</a> structure must contain valid and finite floating-point values.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>endPoint</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The coordinates are relative to the page and are expressed in the units of the transform that is in effect.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomlineargradientbrush">IXpsOMLinearGradientBrush</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>



<a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_point">XPS_POINT</a>