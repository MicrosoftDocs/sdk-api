---
UID: NF:xpsobjectmodel.IXpsOMVisualBrush.SetVisualLookup
title: IXpsOMVisualBrush::SetVisualLookup (xpsobjectmodel.h)
description: Sets the lookup key name of the shared visual, which is stored in a resource dictionary, to be used as the source for the brush.
helpviewer_keywords: ["IXpsOMVisualBrush interface [XPS Documents and Packaging]","SetVisualLookup method","IXpsOMVisualBrush.SetVisualLookup","IXpsOMVisualBrush::SetVisualLookup","SetVisualLookup","SetVisualLookup method [XPS Documents and Packaging]","SetVisualLookup method [XPS Documents and Packaging]","IXpsOMVisualBrush interface","xps.ixpsomvisualbrush_setvisuallookup","xpsobjectmodel/IXpsOMVisualBrush::SetVisualLookup"]
old-location: xps\ixpsomvisualbrush_setvisuallookup.htm
tech.root: xps
ms.assetid: ab98d93c-76fe-477b-9032-c54c0e22a176
ms.date: 12/05/2018
ms.keywords: IXpsOMVisualBrush interface [XPS Documents and Packaging],SetVisualLookup method, IXpsOMVisualBrush.SetVisualLookup, IXpsOMVisualBrush::SetVisualLookup, SetVisualLookup, SetVisualLookup method [XPS Documents and Packaging], SetVisualLookup method [XPS Documents and Packaging],IXpsOMVisualBrush interface, xps.ixpsomvisualbrush_setvisuallookup, xpsobjectmodel/IXpsOMVisualBrush::SetVisualLookup
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
 - IXpsOMVisualBrush::SetVisualLookup
 - xpsobjectmodel/IXpsOMVisualBrush::SetVisualLookup
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
 - IXpsOMVisualBrush.SetVisualLookup
---

# IXpsOMVisualBrush::SetVisualLookup


## -description

Sets the lookup key name of the shared visual, which is stored in a resource dictionary, to be used as the source for the brush.

## -parameters

### -param lookup [in]

The lookup key name of the shared visual to be used as the source for the brush. If a lookup key has already been set, a <b>NULL</b> pointer will clear it.

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

After you call <b>SetVisualLookup</b>, the local visual is released and <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisualbrush-getvisuallocal">GetVisualLocal</a> returns a <b>NULL</b> pointer in the <i>visual</i> parameter. The table that follows explains the relationship between the local and lookup values of this property.


<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned  in <i>visual</i> by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisualbrush-getvisual">GetVisual</a>
</th>
<th>Object that is returned  in <i>visual</i> by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisualbrush-getvisuallocal">GetVisualLocal</a>
</th>
<th>String that is returned  in <i>lookup</i> by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisualbrush-getvisuallookup">GetVisualLookup</a>
</th>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisualbrush-setvisuallocal">SetVisualLocal</a>


</td>
<td>
The visual  that is set by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisualbrush-setvisuallocal">SetVisualLocal</a>.

</td>
<td>
The visual  that is set by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisualbrush-setvisuallocal">SetVisualLocal</a>.

</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
<tr>
<td>
<b>SetVisualLookup</b> (this method).

</td>
<td>
The visual  that is retrieved, with a lookup key that matches the key set by <b>SetVisualLookup</b>, from the resource directory.

</td>
<td>
<b>NULL</b> pointer.

</td>
<td>
The lookup key that is set by <b>SetVisualLookup</b>.

</td>
</tr>
<tr>
<td>
Neither <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisualbrush-setvisuallocal">SetVisualLocal</a> nor <b>SetVisualLookup</b> has been called yet.

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

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush">IXpsOMVisualBrush</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>