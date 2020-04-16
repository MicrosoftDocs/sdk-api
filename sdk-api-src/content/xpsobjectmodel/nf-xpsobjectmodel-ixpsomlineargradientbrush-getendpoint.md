---
UID: NF:xpsobjectmodel.IXpsOMLinearGradientBrush.GetEndPoint
title: IXpsOMLinearGradientBrush::GetEndPoint (xpsobjectmodel.h)
description: Gets the end point of the gradient.helpviewer_keywords: ["GetEndPoint","GetEndPoint method [XPS Documents and Packaging]","GetEndPoint method [XPS Documents and Packaging]","IXpsOMLinearGradientBrush interface","IXpsOMLinearGradientBrush interface [XPS Documents and Packaging]","GetEndPoint method","IXpsOMLinearGradientBrush.GetEndPoint","IXpsOMLinearGradientBrush::GetEndPoint","xps.ixpsomlineargradientbrush_getendpoint","xpsobjectmodel/IXpsOMLinearGradientBrush::GetEndPoint"]
old-location: xps\ixpsomlineargradientbrush_getendpoint.htm
tech.root: printdocs
ms.assetid: c8f34c4b-28f1-4a8f-bf8e-9872debc9eb1
ms.date: 12/05/2018
ms.keywords: GetEndPoint, GetEndPoint method [XPS Documents and Packaging], GetEndPoint method [XPS Documents and Packaging],IXpsOMLinearGradientBrush interface, IXpsOMLinearGradientBrush interface [XPS Documents and Packaging],GetEndPoint method, IXpsOMLinearGradientBrush.GetEndPoint, IXpsOMLinearGradientBrush::GetEndPoint, xps.ixpsomlineargradientbrush_getendpoint, xpsobjectmodel/IXpsOMLinearGradientBrush::GetEndPoint
f1_keywords:
- xpsobjectmodel/IXpsOMLinearGradientBrush.GetEndPoint
dev_langs:
- c++
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
- IXpsOMLinearGradientBrush.GetEndPoint
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMLinearGradientBrush::GetEndPoint


## -description


Gets the end point of the gradient.


## -parameters




### -param endPoint [out, retval]

The x and y coordinates of the end point.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>.

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
<i>endPoint</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The coordinates are relative to the page and are expressed in units of the transform that is in effect.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomlineargradientbrush">IXpsOMLinearGradientBrush</a>



<a href="https://www.microsoft.com/download/details.aspx?id=11816">XML Paper Specification</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>



<a href="https://docs.microsoft.com/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_point">XPS_POINT</a>
 

 

