---
UID: NF:xpsobjectmodel.IXpsOMBrush.SetOpacity
title: IXpsOMBrush::SetOpacity (xpsobjectmodel.h)
description: Sets the opacity of the brush.
helpviewer_keywords: ["IXpsOMBrush interface [XPS Documents and Packaging]","SetOpacity method","IXpsOMBrush.SetOpacity","IXpsOMBrush::SetOpacity","SetOpacity","SetOpacity method [XPS Documents and Packaging]","SetOpacity method [XPS Documents and Packaging]","IXpsOMBrush interface","xps.ixpsombrush_setopacity","xpsobjectmodel/IXpsOMBrush::SetOpacity"]
old-location: xps\ixpsombrush_setopacity.htm
tech.root: xps
ms.assetid: e0249796-298f-4e26-a767-cd57903e5da0
ms.date: 12/05/2018
ms.keywords: IXpsOMBrush interface [XPS Documents and Packaging],SetOpacity method, IXpsOMBrush.SetOpacity, IXpsOMBrush::SetOpacity, SetOpacity, SetOpacity method [XPS Documents and Packaging], SetOpacity method [XPS Documents and Packaging],IXpsOMBrush interface, xps.ixpsombrush_setopacity, xpsobjectmodel/IXpsOMBrush::SetOpacity
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
 - IXpsOMBrush::SetOpacity
 - xpsobjectmodel/IXpsOMBrush::SetOpacity
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
 - IXpsOMBrush.SetOpacity
---

# IXpsOMBrush::SetOpacity


## -description

Sets the opacity of the brush.

## -parameters

### -param opacity [in]

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>opacity</i> is not a valid value. See the Remarks section.

</td>
</tr>
</table>

## -remarks

<i>opacity</i> is expressed as a value between 0.0 and 1.0; 0.0 indicates that the brush is completely transparent, 0.5  that it is 50 percent opaque, and 1.0 that it is completely opaque.

If <i>opacity</i> is less than 0.0 or greater than 1.0, the method  returns an error.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush">IXpsOMBrush</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>