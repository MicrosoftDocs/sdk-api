---
UID: NF:xpsobjectmodel.IXpsOMPath.SetFillBrushLookup
title: IXpsOMPath::SetFillBrushLookup (xpsobjectmodel.h)
description: Sets the lookup key name of a shared brush in a resource dictionary, to be used as the fill brush.
helpviewer_keywords: ["IXpsOMPath interface [XPS Documents and Packaging]","SetFillBrushLookup method","IXpsOMPath.SetFillBrushLookup","IXpsOMPath::SetFillBrushLookup","SetFillBrushLookup","SetFillBrushLookup method [XPS Documents and Packaging]","SetFillBrushLookup method [XPS Documents and Packaging]","IXpsOMPath interface","xps.ixpsompath_setfillbrushlookup","xpsobjectmodel/IXpsOMPath::SetFillBrushLookup"]
old-location: xps\ixpsompath_setfillbrushlookup.htm
tech.root: xps
ms.assetid: 5a02af98-8bfc-4fb2-92b3-15b16b4b69c1
ms.date: 12/05/2018
ms.keywords: IXpsOMPath interface [XPS Documents and Packaging],SetFillBrushLookup method, IXpsOMPath.SetFillBrushLookup, IXpsOMPath::SetFillBrushLookup, SetFillBrushLookup, SetFillBrushLookup method [XPS Documents and Packaging], SetFillBrushLookup method [XPS Documents and Packaging],IXpsOMPath interface, xps.ixpsompath_setfillbrushlookup, xpsobjectmodel/IXpsOMPath::SetFillBrushLookup
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
 - IXpsOMPath::SetFillBrushLookup
 - xpsobjectmodel/IXpsOMPath::SetFillBrushLookup
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
 - IXpsOMPath.SetFillBrushLookup
---

# IXpsOMPath::SetFillBrushLookup


## -description

Sets the lookup key name of a shared brush in a resource dictionary, to be used as the fill brush.

## -parameters

### -param lookup [in]

The key name of the brush in a resource dictionary, to be used as the fill brush.

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
<dt><b>XPS_E_INVALID_RESOURCE_KEY</b></dt>
</dl>
</td>
<td width="60%">
According to the <a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>, the value of <i>lookup</i> is not a valid lookup key string.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_INVALID_LOOKUP_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The lookup key name in <i>lookup</i> references an object that is not a brush.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_LOOKUP_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
No object could be found with a key name that matched the value passed in <i>lookup</i>.

</td>
</tr>
</table>

## -remarks

After you call <b>SetFillBrushLookup</b>, the local fill brush is released and <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getfillbrushlocal">GetFillBrushLocal</a> returns a <b>NULL</b> pointer in the <i>brush</i> parameter. The table that follows explains the relationship between the local and lookup values of this property.

<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned in <i>brush</i> by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getfillbrush">GetFillBrush</a>
</th>
<th>Object that is returned in <i>brush</i>  by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getfillbrushlocal">GetFillBrushLocal</a>
</th>
<th>String that is returned in <i>lookup</i> by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getfillbrushlookup">GetFillBrushLookup</a>
</th>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setfillbrushlocal">SetFillBrushLocal</a>


</td>
<td>
The local brush that is set by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setfillbrushlocal">SetFillBrushLocal</a>.

</td>
<td>
The local brush that is set by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setfillbrushlocal">SetFillBrushLocal</a>.

</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
<tr>
<td>
<b>SetFillBrushLookup</b> (this method)

</td>
<td>
The shared brush retrieved, with a lookup key that matches the key that is set by <b>SetFillBrushLookup</b>, from the resource directory.

</td>
<td>
<b>NULL</b> pointer.

</td>
<td>
The lookup key that is set by <b>SetFillBrushLookup</b>.

</td>
</tr>
<tr>
<td>
Neither <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setfillbrushlocal">SetFillBrushLocal</a> nor <b>SetFillBrushLookup</b> has been called yet.

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

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath">IXpsOMPath</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>