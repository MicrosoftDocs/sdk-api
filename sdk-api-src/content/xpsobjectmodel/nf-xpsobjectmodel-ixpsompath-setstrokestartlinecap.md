---
UID: NF:xpsobjectmodel.IXpsOMPath.SetStrokeStartLineCap
title: IXpsOMPath::SetStrokeStartLineCap (xpsobjectmodel.h)
description: Sets the style of the stroke's line cap at the start of the stroke line.
helpviewer_keywords: ["IXpsOMPath interface [XPS Documents and Packaging]","SetStrokeStartLineCap method","IXpsOMPath.SetStrokeStartLineCap","IXpsOMPath::SetStrokeStartLineCap","SetStrokeStartLineCap","SetStrokeStartLineCap method [XPS Documents and Packaging]","SetStrokeStartLineCap method [XPS Documents and Packaging]","IXpsOMPath interface","xps.ixpsompath_setstrokestartlinecap","xpsobjectmodel/IXpsOMPath::SetStrokeStartLineCap"]
old-location: xps\ixpsompath_setstrokestartlinecap.htm
tech.root: xps
ms.assetid: 2b465775-6eda-49cb-aa9a-091e4d815da3
ms.date: 12/05/2018
ms.keywords: IXpsOMPath interface [XPS Documents and Packaging],SetStrokeStartLineCap method, IXpsOMPath.SetStrokeStartLineCap, IXpsOMPath::SetStrokeStartLineCap, SetStrokeStartLineCap, SetStrokeStartLineCap method [XPS Documents and Packaging], SetStrokeStartLineCap method [XPS Documents and Packaging],IXpsOMPath interface, xps.ixpsompath_setstrokestartlinecap, xpsobjectmodel/IXpsOMPath::SetStrokeStartLineCap
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
 - IXpsOMPath::SetStrokeStartLineCap
 - xpsobjectmodel/IXpsOMPath::SetStrokeStartLineCap
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
 - IXpsOMPath.SetStrokeStartLineCap
---

# IXpsOMPath::SetStrokeStartLineCap


## -description

Sets the style of the stroke's line cap at the  start of the stroke line.

## -parameters

### -param strokeStartLineCap [in]

The <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_line_cap">XPS_LINE_CAP</a> value to be set.

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
<dt><b>E_INVALIDARG </b></dt>
</dl>
</td>
<td width="60%">
<i>strokeStartLineCap</i> is not a valid <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_line_cap">XPS_LINE_CAP</a> value.

</td>
</tr>
</table>

## -remarks

For more information about the line join styles, see <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_line_cap">XPS_LINE_CAP</a>.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath">IXpsOMPath</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>