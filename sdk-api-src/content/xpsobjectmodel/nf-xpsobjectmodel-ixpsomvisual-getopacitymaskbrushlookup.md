---
UID: NF:xpsobjectmodel.IXpsOMVisual.GetOpacityMaskBrushLookup
title: IXpsOMVisual::GetOpacityMaskBrushLookup (xpsobjectmodel.h)
description: Gets the name of the lookup key of the shared opacity mask brush in a resource dictionary.
helpviewer_keywords: ["GetOpacityMaskBrushLookup","GetOpacityMaskBrushLookup method [XPS Documents and Packaging]","GetOpacityMaskBrushLookup method [XPS Documents and Packaging]","IXpsOMVisual interface","IXpsOMVisual interface [XPS Documents and Packaging]","GetOpacityMaskBrushLookup method","IXpsOMVisual.GetOpacityMaskBrushLookup","IXpsOMVisual::GetOpacityMaskBrushLookup","xps.ixpsomvisual_getopacitymaskbrushlookup","xpsobjectmodel/IXpsOMVisual::GetOpacityMaskBrushLookup"]
old-location: xps\ixpsomvisual_getopacitymaskbrushlookup.htm
tech.root: xps
ms.assetid: 84d4aae9-e3e3-4c82-8877-b8206d3678f0
ms.date: 12/05/2018
ms.keywords: GetOpacityMaskBrushLookup, GetOpacityMaskBrushLookup method [XPS Documents and Packaging], GetOpacityMaskBrushLookup method [XPS Documents and Packaging],IXpsOMVisual interface, IXpsOMVisual interface [XPS Documents and Packaging],GetOpacityMaskBrushLookup method, IXpsOMVisual.GetOpacityMaskBrushLookup, IXpsOMVisual::GetOpacityMaskBrushLookup, xps.ixpsomvisual_getopacitymaskbrushlookup, xpsobjectmodel/IXpsOMVisual::GetOpacityMaskBrushLookup
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
 - IXpsOMVisual::GetOpacityMaskBrushLookup
 - xpsobjectmodel/IXpsOMVisual::GetOpacityMaskBrushLookup
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
 - IXpsOMVisual.GetOpacityMaskBrushLookup
---

# IXpsOMVisual::GetOpacityMaskBrushLookup


## -description

Gets the name of the lookup key of the  shared opacity mask brush in a resource dictionary.

## -parameters

### -param key [out, retval]

The name of the lookup key  of the shared opacity mask brush in a resource dictionary. If the lookup key of an opacity mask brush  has not been set, or if a local opacity mask brush has been set, a <b>NULL</b> pointer is returned.

<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned in <i>key</i></th>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisual-setopacitymaskbrushlocal">SetOpacityMaskBrushLocal</a>


</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisual-setopacitymaskbrushlookup">SetOpacityMaskBrushLookup</a>


</td>
<td>
The lookup key that is set by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisual-setopacitymaskbrushlookup">SetOpacityMaskBrushLookup</a>.

</td>
</tr>
<tr>
<td>
Neither <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisual-setopacitymaskbrushlocal">SetOpacityMaskBrushLocal</a> nor <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisual-setopacitymaskbrushlookup">SetOpacityMaskBrushLookup</a> has been called yet.

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
<i>key</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

This method allocates the memory that is used by the string returned in <i>key</i>.  If <i>key</i> is not <b>NULL</b>, use the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function  to free the memory.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush">IXpsOMBrush</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual">IXpsOMVisual</a>



<a href="https://www.microsoft.com/download/details.aspx?id=11816">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>