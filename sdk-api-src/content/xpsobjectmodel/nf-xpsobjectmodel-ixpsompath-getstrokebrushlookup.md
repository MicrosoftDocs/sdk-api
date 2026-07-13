---
UID: NF:xpsobjectmodel.IXpsOMPath.GetStrokeBrushLookup
title: IXpsOMPath::GetStrokeBrushLookup (xpsobjectmodel.h)
description: Gets the lookup key of the brush that is stored in a resource dictionary and is to be used as the stroke brush for the path.
helpviewer_keywords: ["GetStrokeBrushLookup","GetStrokeBrushLookup method [XPS Documents and Packaging]","GetStrokeBrushLookup method [XPS Documents and Packaging]","IXpsOMPath interface","IXpsOMPath interface [XPS Documents and Packaging]","GetStrokeBrushLookup method","IXpsOMPath.GetStrokeBrushLookup","IXpsOMPath::GetStrokeBrushLookup","xps.ixpsompath_getstrokebrushlookup","xpsobjectmodel/IXpsOMPath::GetStrokeBrushLookup"]
old-location: xps\ixpsompath_getstrokebrushlookup.htm
tech.root: xps
ms.assetid: af70b6a3-203a-4189-b44d-763539e0302a
ms.date: 12/05/2018
ms.keywords: GetStrokeBrushLookup, GetStrokeBrushLookup method [XPS Documents and Packaging], GetStrokeBrushLookup method [XPS Documents and Packaging],IXpsOMPath interface, IXpsOMPath interface [XPS Documents and Packaging],GetStrokeBrushLookup method, IXpsOMPath.GetStrokeBrushLookup, IXpsOMPath::GetStrokeBrushLookup, xps.ixpsompath_getstrokebrushlookup, xpsobjectmodel/IXpsOMPath::GetStrokeBrushLookup
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
 - IXpsOMPath::GetStrokeBrushLookup
 - xpsobjectmodel/IXpsOMPath::GetStrokeBrushLookup
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
 - IXpsOMPath.GetStrokeBrushLookup
---

# IXpsOMPath::GetStrokeBrushLookup


## -description

Gets the lookup key of the brush  that is stored in a resource dictionary and is to be used as the stroke brush for the path.

## -parameters

### -param lookup [out, retval]

The lookup key of a brush that is stored in a resource dictionary. If a stroke brush lookup key has not been set or if a local stroke brush has been set, a <b>NULL</b> pointer is returned.

<table>
<tr>
<th>Most recent method called</th>
<th>String that is returned in <i>lookup</i></th>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlocal">SetStrokeBrushLocal</a>


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
The lookup key that is set by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlookup">SetStrokeBrushLookup</a>.

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
<i>lookup</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

This method allocates the memory used by the string that is returned in <i>lookup</i>.  If <i>lookup</i> is not <b>NULL</b>, use the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function  to free the memory.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath">IXpsOMPath</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>