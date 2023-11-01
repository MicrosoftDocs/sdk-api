---
UID: NF:xpsobjectmodel.IXpsOMPath.SetStrokeBrushLocal
title: IXpsOMPath::SetStrokeBrushLocal (xpsobjectmodel.h)
description: Sets a pointer to a local, unshared IXpsOMBrush interface to be used as a stroke brush.
helpviewer_keywords: ["IXpsOMPath interface [XPS Documents and Packaging]","SetStrokeBrushLocal method","IXpsOMPath.SetStrokeBrushLocal","IXpsOMPath::SetStrokeBrushLocal","SetStrokeBrushLocal","SetStrokeBrushLocal method [XPS Documents and Packaging]","SetStrokeBrushLocal method [XPS Documents and Packaging]","IXpsOMPath interface","xps.ixpsompath_setstrokebrushlocal","xpsobjectmodel/IXpsOMPath::SetStrokeBrushLocal"]
old-location: xps\ixpsompath_setstrokebrushlocal.htm
tech.root: xps
ms.assetid: 551bc4e2-2bf3-455b-a7f1-35b3b66697c0
ms.date: 12/05/2018
ms.keywords: IXpsOMPath interface [XPS Documents and Packaging],SetStrokeBrushLocal method, IXpsOMPath.SetStrokeBrushLocal, IXpsOMPath::SetStrokeBrushLocal, SetStrokeBrushLocal, SetStrokeBrushLocal method [XPS Documents and Packaging], SetStrokeBrushLocal method [XPS Documents and Packaging],IXpsOMPath interface, xps.ixpsompath_setstrokebrushlocal, xpsobjectmodel/IXpsOMPath::SetStrokeBrushLocal
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
 - IXpsOMPath::SetStrokeBrushLocal
 - xpsobjectmodel/IXpsOMPath::SetStrokeBrushLocal
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
 - IXpsOMPath.SetStrokeBrushLocal
---

# IXpsOMPath::SetStrokeBrushLocal


## -description

Sets a pointer to a local, unshared <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush">IXpsOMBrush</a> interface to be used as a stroke brush.

## -parameters

### -param brush [in]

A pointer to a local, unshared <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush">IXpsOMBrush</a> interface to be used as a stroke brush.

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
<dt><b>XPS_E_NO_CUSTOM_OBJECTS</b></dt>
</dl>
</td>
<td width="60%">
<i>brush</i> does not point to a recognized interface implementation. Custom implementation of XPS Document API interfaces is not supported.

</td>
</tr>
</table>

## -remarks

After you call <b>SetStrokeBrushLocal</b>, the stroke brush lookup key is released and <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getstrokebrushlookup">GetStrokeBrushLookup</a> returns a <b>NULL</b> pointer in the <i>lookup</i> parameter. The table that follows explains the relationship between the local and lookup values of this property.

<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned in <i>brush</i> by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getstrokebrush">GetStrokeBrush</a>
</th>
<th>Object that is returned in <i>brush</i> by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getstrokebrushlocal">GetStrokeBrushLocal</a>
</th>
<th>String that is returned in <i>lookup</i> by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getstrokebrushlookup">GetStrokeBrushLookup</a>
</th>
</tr>
<tr>
<td>
<b>SetStrokeBrushLocal</b>  (this method)

</td>
<td>
The local brush that is set by <b>SetStrokeBrushLocal</b>.

</td>
<td>
The local brush that is set by <b>SetStrokeBrushLocal</b>.

</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlookup">SetStrokeBrushLookup</a>


</td>
<td>
The shared brush retrieved, with a lookup key that matches the key set by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlookup">SetStrokeBrushLookup</a>, from the resource directory.

</td>
<td>
<b>NULL</b> pointer.

</td>
<td>
The lookup key that is set by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlookup">SetStrokeBrushLookup</a>.

</td>
</tr>
<tr>
<td>
Neither <b>SetStrokeBrushLocal</b> nor <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlookup">SetStrokeBrushLookup</a> has been called yet.

</td>
<td>
<b>NULL</b> pointer.

</td>
<td>
<b>NULL</b> pointer.

</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush">IXpsOMBrush</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath">IXpsOMPath</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>