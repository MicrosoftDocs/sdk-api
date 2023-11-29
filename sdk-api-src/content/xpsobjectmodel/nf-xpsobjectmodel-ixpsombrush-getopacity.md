---
UID: NF:xpsobjectmodel.IXpsOMBrush.GetOpacity
title: IXpsOMBrush::GetOpacity (xpsobjectmodel.h)
description: Gets the opacity of the brush.
helpviewer_keywords: ["GetOpacity","GetOpacity method [XPS Documents and Packaging]","GetOpacity method [XPS Documents and Packaging]","IXpsOMBrush interface","IXpsOMBrush interface [XPS Documents and Packaging]","GetOpacity method","IXpsOMBrush.GetOpacity","IXpsOMBrush::GetOpacity","xps.ixpsombrush_getopacity","xpsobjectmodel/IXpsOMBrush::GetOpacity"]
old-location: xps\ixpsombrush_getopacity.htm
tech.root: xps
ms.assetid: 53819ce0-4b81-4720-8c1d-6e9031b228c9
ms.date: 12/05/2018
ms.keywords: GetOpacity, GetOpacity method [XPS Documents and Packaging], GetOpacity method [XPS Documents and Packaging],IXpsOMBrush interface, IXpsOMBrush interface [XPS Documents and Packaging],GetOpacity method, IXpsOMBrush.GetOpacity, IXpsOMBrush::GetOpacity, xps.ixpsombrush_getopacity, xpsobjectmodel/IXpsOMBrush::GetOpacity
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
 - IXpsOMBrush::GetOpacity
 - xpsobjectmodel/IXpsOMBrush::GetOpacity
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
 - IXpsOMBrush.GetOpacity
---

# IXpsOMBrush::GetOpacity


## -description

Gets the opacity of the brush.

## -parameters

### -param opacity [out, retval]

The opacity value of the brush.

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
<i>opacity</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

<i>opacity</i> is expressed as a value between 0.0 and 1.0; 0.0 indicates that the brush is completely transparent, 0.5  that it is 50 percent opaque, and 1.0 that it is completely opaque.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush">IXpsOMBrush</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>