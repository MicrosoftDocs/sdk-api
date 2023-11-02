---
UID: NF:xpsobjectmodel.IXpsOMPath.SetStrokeEndLineCap
title: IXpsOMPath::SetStrokeEndLineCap (xpsobjectmodel.h)
description: Sets the style of the stroke line's end cap.
helpviewer_keywords: ["IXpsOMPath interface [XPS Documents and Packaging]","SetStrokeEndLineCap method","IXpsOMPath.SetStrokeEndLineCap","IXpsOMPath::SetStrokeEndLineCap","SetStrokeEndLineCap","SetStrokeEndLineCap method [XPS Documents and Packaging]","SetStrokeEndLineCap method [XPS Documents and Packaging]","IXpsOMPath interface","xps.ixpsompath_setstrokeendlinecap","xpsobjectmodel/IXpsOMPath::SetStrokeEndLineCap"]
old-location: xps\ixpsompath_setstrokeendlinecap.htm
tech.root: xps
ms.assetid: f223503c-4934-4b3d-b489-c8f6488b05d0
ms.date: 12/05/2018
ms.keywords: IXpsOMPath interface [XPS Documents and Packaging],SetStrokeEndLineCap method, IXpsOMPath.SetStrokeEndLineCap, IXpsOMPath::SetStrokeEndLineCap, SetStrokeEndLineCap, SetStrokeEndLineCap method [XPS Documents and Packaging], SetStrokeEndLineCap method [XPS Documents and Packaging],IXpsOMPath interface, xps.ixpsompath_setstrokeendlinecap, xpsobjectmodel/IXpsOMPath::SetStrokeEndLineCap
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
 - IXpsOMPath::SetStrokeEndLineCap
 - xpsobjectmodel/IXpsOMPath::SetStrokeEndLineCap
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
 - IXpsOMPath.SetStrokeEndLineCap
---

# IXpsOMPath::SetStrokeEndLineCap


## -description

Sets the style of the stroke line's end cap.

## -parameters

### -param strokeEndLineCap [in]

The <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_line_cap">XPS_LINE_CAP</a> value to be  set.

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
<i>strokeEndLineCap</i> is not a valid <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_line_cap">XPS_LINE_CAP</a> value.

</td>
</tr>
</table>

## -remarks

For more information about dash cap styles, see <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_line_cap">XPS_LINE_CAP</a>.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath">IXpsOMPath</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>