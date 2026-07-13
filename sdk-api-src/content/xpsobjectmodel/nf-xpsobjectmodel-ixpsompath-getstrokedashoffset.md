---
UID: NF:xpsobjectmodel.IXpsOMPath.GetStrokeDashOffset
title: IXpsOMPath::GetStrokeDashOffset (xpsobjectmodel.h)
description: Gets the offset from the origin of the stroke to the starting point of the dash array pattern.
helpviewer_keywords: ["GetStrokeDashOffset","GetStrokeDashOffset method [XPS Documents and Packaging]","GetStrokeDashOffset method [XPS Documents and Packaging]","IXpsOMPath interface","IXpsOMPath interface [XPS Documents and Packaging]","GetStrokeDashOffset method","IXpsOMPath.GetStrokeDashOffset","IXpsOMPath::GetStrokeDashOffset","xps.ixpsompath_getstrokedashoffset","xpsobjectmodel/IXpsOMPath::GetStrokeDashOffset"]
old-location: xps\ixpsompath_getstrokedashoffset.htm
tech.root: xps
ms.assetid: 173e820f-e926-44cc-a6ba-54edde770f73
ms.date: 12/05/2018
ms.keywords: GetStrokeDashOffset, GetStrokeDashOffset method [XPS Documents and Packaging], GetStrokeDashOffset method [XPS Documents and Packaging],IXpsOMPath interface, IXpsOMPath interface [XPS Documents and Packaging],GetStrokeDashOffset method, IXpsOMPath.GetStrokeDashOffset, IXpsOMPath::GetStrokeDashOffset, xps.ixpsompath_getstrokedashoffset, xpsobjectmodel/IXpsOMPath::GetStrokeDashOffset
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
 - IXpsOMPath::GetStrokeDashOffset
 - xpsobjectmodel/IXpsOMPath::GetStrokeDashOffset
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
 - IXpsOMPath.GetStrokeDashOffset
---

# IXpsOMPath::GetStrokeDashOffset


## -description

Gets the offset from the origin of the stroke to the starting point of the dash array pattern.

## -parameters

### -param strokeDashOffset [out, retval]

The offset value; specified in multiples of the stroke thickness.

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
<i>strokeDashOffset</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath">IXpsOMPath</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>