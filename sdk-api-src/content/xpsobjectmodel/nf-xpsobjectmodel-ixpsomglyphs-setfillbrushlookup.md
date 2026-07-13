---
UID: NF:xpsobjectmodel.IXpsOMGlyphs.SetFillBrushLookup
title: IXpsOMGlyphs::SetFillBrushLookup (xpsobjectmodel.h)
description: Sets the lookup key name of a shared fill brush.
helpviewer_keywords: ["IXpsOMGlyphs interface [XPS Documents and Packaging]","SetFillBrushLookup method","IXpsOMGlyphs.SetFillBrushLookup","IXpsOMGlyphs::SetFillBrushLookup","SetFillBrushLookup","SetFillBrushLookup method [XPS Documents and Packaging]","SetFillBrushLookup method [XPS Documents and Packaging]","IXpsOMGlyphs interface","xps.ixpsomglyphs_setfillbrushlookup","xpsobjectmodel/IXpsOMGlyphs::SetFillBrushLookup"]
old-location: xps\ixpsomglyphs_setfillbrushlookup.htm
tech.root: xps
ms.assetid: a983583b-8698-48aa-af24-2e71d87d30c4
ms.date: 12/05/2018
ms.keywords: IXpsOMGlyphs interface [XPS Documents and Packaging],SetFillBrushLookup method, IXpsOMGlyphs.SetFillBrushLookup, IXpsOMGlyphs::SetFillBrushLookup, SetFillBrushLookup, SetFillBrushLookup method [XPS Documents and Packaging], SetFillBrushLookup method [XPS Documents and Packaging],IXpsOMGlyphs interface, xps.ixpsomglyphs_setfillbrushlookup, xpsobjectmodel/IXpsOMGlyphs::SetFillBrushLookup
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
 - IXpsOMGlyphs::SetFillBrushLookup
 - xpsobjectmodel/IXpsOMGlyphs::SetFillBrushLookup
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
 - IXpsOMGlyphs.SetFillBrushLookup
---

# IXpsOMGlyphs::SetFillBrushLookup


## -description

Sets the lookup key name of a shared fill brush.

## -parameters

### -param key [in]

A string variable that contains the key name of the fill brush that is stored in the resource dictionary and will be used as the shared fill brush. A <b>NULL</b> pointer clears any previously assigned key string.

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
The lookup key name in <i>key</i> references an object that is not a geometry.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_LOOKUP_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
No object could be found with a key name that matched the value passed in <i>key</i>.

</td>
</tr>
</table>

## -remarks

After you call <b>SetFillBrushLookup</b>, the local fill brush is released and <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphs-getfillbrushlocal">GetFillBrushLocal</a> returns a <b>NULL</b> pointer in the <i>fillBrush</i> parameter. The table that follows explains the relationship between the local and lookup values of this property.

<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned in <i>fillBrush</i> by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphs-getfillbrush">GetFillBrush</a>
</th>
<th>Object that is returned in <i>fillBrush</i>   by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphs-getfillbrushlocal">GetFillBrushLocal</a>
</th>
<th>String that is returned in <i>key</i> by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphs-getfillbrushlookup">GetFillBrushLookup</a>
</th>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphs-setfillbrushlocal">SetFillBrushLocal</a>


</td>
<td>
The local brush that is set by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphs-setfillbrushlocal">SetFillBrushLocal</a>.

</td>
<td>
The local brush that is set by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphs-setfillbrushlocal">SetFillBrushLocal</a>.

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
The shared brush that gets retrieved, with a lookup key matching the key that is set by <b>SetFillBrushLookup</b>, from the resource directory.

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
Neither <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphs-setfillbrushlocal">SetFillBrushLocal</a> nor <b>SetFillBrushLookup</b> has been called yet.

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

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs">IXpsOMGlyphs</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>