---
UID: NF:xpsobjectmodel.IXpsOMLinearGradientBrush.GetStartPoint
title: IXpsOMLinearGradientBrush::GetStartPoint (xpsobjectmodel.h)
description: Gets the start point of the gradient.
helpviewer_keywords: ["GetStartPoint","GetStartPoint method [XPS Documents and Packaging]","GetStartPoint method [XPS Documents and Packaging]","IXpsOMLinearGradientBrush interface","IXpsOMLinearGradientBrush interface [XPS Documents and Packaging]","GetStartPoint method","IXpsOMLinearGradientBrush.GetStartPoint","IXpsOMLinearGradientBrush::GetStartPoint","xps.ixpsomlineargradientbrush_getstartpoint","xpsobjectmodel/IXpsOMLinearGradientBrush::GetStartPoint"]
old-location: xps\ixpsomlineargradientbrush_getstartpoint.htm
tech.root: xps
ms.assetid: 03e9884b-6249-4ccb-a6ee-d360655c5f75
ms.date: 12/05/2018
ms.keywords: GetStartPoint, GetStartPoint method [XPS Documents and Packaging], GetStartPoint method [XPS Documents and Packaging],IXpsOMLinearGradientBrush interface, IXpsOMLinearGradientBrush interface [XPS Documents and Packaging],GetStartPoint method, IXpsOMLinearGradientBrush.GetStartPoint, IXpsOMLinearGradientBrush::GetStartPoint, xps.ixpsomlineargradientbrush_getstartpoint, xpsobjectmodel/IXpsOMLinearGradientBrush::GetStartPoint
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
 - IXpsOMLinearGradientBrush::GetStartPoint
 - xpsobjectmodel/IXpsOMLinearGradientBrush::GetStartPoint
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
 - IXpsOMLinearGradientBrush.GetStartPoint
---

# IXpsOMLinearGradientBrush::GetStartPoint


## -description

Gets the start point of the gradient.

## -parameters

### -param startPoint [out, retval]

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>startPoint</i> is <b>NULL</b>.

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