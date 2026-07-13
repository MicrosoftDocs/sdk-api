---
UID: NF:xpsobjectmodel.IXpsOMVisual.GetOpacity
title: IXpsOMVisual::GetOpacity (xpsobjectmodel.h)
description: Gets the opacity value of this visual.
helpviewer_keywords: ["GetOpacity","GetOpacity method [XPS Documents and Packaging]","GetOpacity method [XPS Documents and Packaging]","IXpsOMVisual interface","IXpsOMVisual interface [XPS Documents and Packaging]","GetOpacity method","IXpsOMVisual.GetOpacity","IXpsOMVisual::GetOpacity","xps.ixpsomvisual_getopacity","xpsobjectmodel/IXpsOMVisual::GetOpacity"]
old-location: xps\ixpsomvisual_getopacity.htm
tech.root: xps
ms.assetid: c513ea28-937a-4594-9a50-0c7999f435ce
ms.date: 12/05/2018
ms.keywords: GetOpacity, GetOpacity method [XPS Documents and Packaging], GetOpacity method [XPS Documents and Packaging],IXpsOMVisual interface, IXpsOMVisual interface [XPS Documents and Packaging],GetOpacity method, IXpsOMVisual.GetOpacity, IXpsOMVisual::GetOpacity, xps.ixpsomvisual_getopacity, xpsobjectmodel/IXpsOMVisual::GetOpacity
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
 - IXpsOMVisual::GetOpacity
 - xpsobjectmodel/IXpsOMVisual::GetOpacity
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
 - IXpsOMVisual.GetOpacity
---

# IXpsOMVisual::GetOpacity


## -description

Gets the opacity value of this visual.

## -parameters

### -param opacity [out, retval]

The opacity value.

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

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual">IXpsOMVisual</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>