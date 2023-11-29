---
UID: NF:xpsobjectmodel.IXpsOMPath.SetStrokeMiterLimit
title: IXpsOMPath::SetStrokeMiterLimit (xpsobjectmodel.h)
description: Sets the miter limit of the path.
helpviewer_keywords: ["IXpsOMPath interface [XPS Documents and Packaging]","SetStrokeMiterLimit method","IXpsOMPath.SetStrokeMiterLimit","IXpsOMPath::SetStrokeMiterLimit","SetStrokeMiterLimit","SetStrokeMiterLimit method [XPS Documents and Packaging]","SetStrokeMiterLimit method [XPS Documents and Packaging]","IXpsOMPath interface","xps.ixpsompath_setstrokemiterlimit","xpsobjectmodel/IXpsOMPath::SetStrokeMiterLimit"]
old-location: xps\ixpsompath_setstrokemiterlimit.htm
tech.root: xps
ms.assetid: 4e33f9f3-119a-4635-b44c-fa002a59fa20
ms.date: 12/05/2018
ms.keywords: IXpsOMPath interface [XPS Documents and Packaging],SetStrokeMiterLimit method, IXpsOMPath.SetStrokeMiterLimit, IXpsOMPath::SetStrokeMiterLimit, SetStrokeMiterLimit, SetStrokeMiterLimit method [XPS Documents and Packaging], SetStrokeMiterLimit method [XPS Documents and Packaging],IXpsOMPath interface, xps.ixpsompath_setstrokemiterlimit, xpsobjectmodel/IXpsOMPath::SetStrokeMiterLimit
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
 - IXpsOMPath::SetStrokeMiterLimit
 - xpsobjectmodel/IXpsOMPath::SetStrokeMiterLimit
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
 - IXpsOMPath.SetStrokeMiterLimit
---

# IXpsOMPath::SetStrokeMiterLimit


## -description

Sets the miter limit of the path.

## -parameters

### -param strokeMiterLimit [in]

The miter limit value to be set. The value must be 1.0 or greater.

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
A value that was passed in <i>strokeMiterLimit</i> was not valid.

</td>
</tr>
</table>

## -remarks

 The miter limit value is the ratio of the maximum miter length  to one-half of the stroke thickness.

The miter limit value describes how to render a mitered line join. This value applies only if the line join style value is <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_line_join">XPS_LINE_JOIN_MITER</a>.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath">IXpsOMPath</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>