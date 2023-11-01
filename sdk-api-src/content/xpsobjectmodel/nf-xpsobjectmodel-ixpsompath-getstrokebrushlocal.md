---
UID: NF:xpsobjectmodel.IXpsOMPath.GetStrokeBrushLocal
title: IXpsOMPath::GetStrokeBrushLocal (xpsobjectmodel.h)
description: Gets a pointer to the local, unshared IXpsOMBrush interface that contains the stroke brush for the path.
helpviewer_keywords: ["GetStrokeBrushLocal","GetStrokeBrushLocal method [XPS Documents and Packaging]","GetStrokeBrushLocal method [XPS Documents and Packaging]","IXpsOMPath interface","IXpsOMPath interface [XPS Documents and Packaging]","GetStrokeBrushLocal method","IXpsOMPath.GetStrokeBrushLocal","IXpsOMPath::GetStrokeBrushLocal","xps.ixpsompath_getstrokebrushlocal","xpsobjectmodel/IXpsOMPath::GetStrokeBrushLocal"]
old-location: xps\ixpsompath_getstrokebrushlocal.htm
tech.root: xps
ms.assetid: cf816750-8381-4c04-af20-e5ce3f8ad63c
ms.date: 12/05/2018
ms.keywords: GetStrokeBrushLocal, GetStrokeBrushLocal method [XPS Documents and Packaging], GetStrokeBrushLocal method [XPS Documents and Packaging],IXpsOMPath interface, IXpsOMPath interface [XPS Documents and Packaging],GetStrokeBrushLocal method, IXpsOMPath.GetStrokeBrushLocal, IXpsOMPath::GetStrokeBrushLocal, xps.ixpsompath_getstrokebrushlocal, xpsobjectmodel/IXpsOMPath::GetStrokeBrushLocal
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
 - IXpsOMPath::GetStrokeBrushLocal
 - xpsobjectmodel/IXpsOMPath::GetStrokeBrushLocal
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
 - IXpsOMPath.GetStrokeBrushLocal
---

# IXpsOMPath::GetStrokeBrushLocal


## -description

Gets a pointer to the local, unshared <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush">IXpsOMBrush</a> interface that contains the stroke brush for the path.

## -parameters

### -param brush [out, retval]

The local, unshared <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush">IXpsOMBrush</a> interface that contains the stroke brush for the path. If a stroke brush lookup key has been set or if a local stroke brush has not been set, a <b>NULL</b> pointer is returned.



<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned in <i>brush</i></th>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlocal">SetStrokeBrushLocal</a>


</td>
<td>
The local brush that is set by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlocal">SetStrokeBrushLocal</a>.

</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlookup">SetStrokeBrushLookup</a>


</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
<tr>
<td>
Neither <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlocal">SetStrokeBrushLocal</a> nor <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlookup">SetStrokeBrushLookup</a> has been called yet.

</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
</table>

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
<i>brush</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush">IXpsOMBrush</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath">IXpsOMPath</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>