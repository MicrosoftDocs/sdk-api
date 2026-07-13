---
UID: NF:xpsobjectmodel.IXpsOMLinearGradientBrush.SetStartPoint
title: IXpsOMLinearGradientBrush::SetStartPoint (xpsobjectmodel.h)
description: Sets the start point of the gradient.
helpviewer_keywords: ["IXpsOMLinearGradientBrush interface [XPS Documents and Packaging]","SetStartPoint method","IXpsOMLinearGradientBrush.SetStartPoint","IXpsOMLinearGradientBrush::SetStartPoint","SetStartPoint","SetStartPoint method [XPS Documents and Packaging]","SetStartPoint method [XPS Documents and Packaging]","IXpsOMLinearGradientBrush interface","xps.ixpsomlineargradientbrush_setstartpoint","xpsobjectmodel/IXpsOMLinearGradientBrush::SetStartPoint"]
old-location: xps\ixpsomlineargradientbrush_setstartpoint.htm
tech.root: xps
ms.assetid: f2e40d75-c0de-4cba-850d-0c8c328e2950
ms.date: 12/05/2018
ms.keywords: IXpsOMLinearGradientBrush interface [XPS Documents and Packaging],SetStartPoint method, IXpsOMLinearGradientBrush.SetStartPoint, IXpsOMLinearGradientBrush::SetStartPoint, SetStartPoint, SetStartPoint method [XPS Documents and Packaging], SetStartPoint method [XPS Documents and Packaging],IXpsOMLinearGradientBrush interface, xps.ixpsomlineargradientbrush_setstartpoint, xpsobjectmodel/IXpsOMLinearGradientBrush::SetStartPoint
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
 - IXpsOMLinearGradientBrush::SetStartPoint
 - xpsobjectmodel/IXpsOMLinearGradientBrush::SetStartPoint
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
 - IXpsOMLinearGradientBrush.SetStartPoint
---

# IXpsOMLinearGradientBrush::SetStartPoint


## -description

Sets the start point of the gradient.

## -parameters

### -param startPoint [in]

The x and y coordinates of the start point.

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
The point described by <i>startPoint</i> was not valid. The <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_point">XPS_POINT</a> structure must contain valid and finite floating-point values.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>startPoint</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The coordinates are relative to the page and are expressed in the units of the  transform that is in effect.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomlineargradientbrush">IXpsOMLinearGradientBrush</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>



<a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_point">XPS_POINT</a>