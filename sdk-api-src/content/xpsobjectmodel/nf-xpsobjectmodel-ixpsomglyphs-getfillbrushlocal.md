---
UID: NF:xpsobjectmodel.IXpsOMGlyphs.GetFillBrushLocal
title: IXpsOMGlyphs::GetFillBrushLocal (xpsobjectmodel.h)
description: Gets a pointer to the local, unshared IXpsOMBrush interface of the fill brush to be used for the text.
helpviewer_keywords: ["GetFillBrushLocal","GetFillBrushLocal method [XPS Documents and Packaging]","GetFillBrushLocal method [XPS Documents and Packaging]","IXpsOMGlyphs interface","IXpsOMGlyphs interface [XPS Documents and Packaging]","GetFillBrushLocal method","IXpsOMGlyphs.GetFillBrushLocal","IXpsOMGlyphs::GetFillBrushLocal","xps.ixpsomglyphs_getfillbrushlocal","xpsobjectmodel/IXpsOMGlyphs::GetFillBrushLocal"]
old-location: xps\ixpsomglyphs_getfillbrushlocal.htm
tech.root: xps
ms.assetid: d497eac9-8096-4a0e-bb43-315f734fd36e
ms.date: 12/05/2018
ms.keywords: GetFillBrushLocal, GetFillBrushLocal method [XPS Documents and Packaging], GetFillBrushLocal method [XPS Documents and Packaging],IXpsOMGlyphs interface, IXpsOMGlyphs interface [XPS Documents and Packaging],GetFillBrushLocal method, IXpsOMGlyphs.GetFillBrushLocal, IXpsOMGlyphs::GetFillBrushLocal, xps.ixpsomglyphs_getfillbrushlocal, xpsobjectmodel/IXpsOMGlyphs::GetFillBrushLocal
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
 - IXpsOMGlyphs::GetFillBrushLocal
 - xpsobjectmodel/IXpsOMGlyphs::GetFillBrushLocal
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
 - IXpsOMGlyphs.GetFillBrushLocal
---

# IXpsOMGlyphs::GetFillBrushLocal


## -description

Gets a pointer to the  local, unshared <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush">IXpsOMBrush</a> interface of  the fill brush to be used for the text.

## -parameters

### -param fillBrush [out, retval]

A pointer to the local, unshared <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush">IXpsOMBrush</a> interface of the  fill brush to be used for the text. If a fill brush lookup key has been set or if a local fill brush has not been set, a <b>NULL</b> pointer will be returned.

<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned in <i>fillBrush</i></th>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphs-setfillbrushlocal">SetFillBrushLocal</a>


</td>
<td>
The local brush that is set by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphs-setfillbrushlocal">SetFillBrushLocal</a>.

</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphs-setfillbrushlookup">SetFillBrushLookup</a>


</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
<tr>
<td>
Neither <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphs-setfillbrushlocal">SetFillBrushLocal</a> nor <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphs-setfillbrushlookup">SetFillBrushLookup</a> has been called yet.

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
<i>fillBrush</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush">IXpsOMBrush</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs">IXpsOMGlyphs</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>