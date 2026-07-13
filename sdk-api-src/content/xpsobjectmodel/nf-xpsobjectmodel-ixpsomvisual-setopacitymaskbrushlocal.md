---
UID: NF:xpsobjectmodel.IXpsOMVisual.SetOpacityMaskBrushLocal
title: IXpsOMVisual::SetOpacityMaskBrushLocal (xpsobjectmodel.h)
description: Sets the IXpsOMBrush interface pointer as the local, unshared opacity mask brush.
helpviewer_keywords: ["IXpsOMVisual interface [XPS Documents and Packaging]","SetOpacityMaskBrushLocal method","IXpsOMVisual.SetOpacityMaskBrushLocal","IXpsOMVisual::SetOpacityMaskBrushLocal","SetOpacityMaskBrushLocal","SetOpacityMaskBrushLocal method [XPS Documents and Packaging]","SetOpacityMaskBrushLocal method [XPS Documents and Packaging]","IXpsOMVisual interface","xps.ixpsomvisual_setopacitymaskbrushlocal","xpsobjectmodel/IXpsOMVisual::SetOpacityMaskBrushLocal"]
old-location: xps\ixpsomvisual_setopacitymaskbrushlocal.htm
tech.root: xps
ms.assetid: d1b84156-b7ad-4dac-97d9-60aaedcee210
ms.date: 12/05/2018
ms.keywords: IXpsOMVisual interface [XPS Documents and Packaging],SetOpacityMaskBrushLocal method, IXpsOMVisual.SetOpacityMaskBrushLocal, IXpsOMVisual::SetOpacityMaskBrushLocal, SetOpacityMaskBrushLocal, SetOpacityMaskBrushLocal method [XPS Documents and Packaging], SetOpacityMaskBrushLocal method [XPS Documents and Packaging],IXpsOMVisual interface, xps.ixpsomvisual_setopacitymaskbrushlocal, xpsobjectmodel/IXpsOMVisual::SetOpacityMaskBrushLocal
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
 - IXpsOMVisual::SetOpacityMaskBrushLocal
 - xpsobjectmodel/IXpsOMVisual::SetOpacityMaskBrushLocal
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
 - IXpsOMVisual.SetOpacityMaskBrushLocal
---

# IXpsOMVisual::SetOpacityMaskBrushLocal


## -description

Sets the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush">IXpsOMBrush</a> interface pointer as the local, unshared opacity mask brush.

## -parameters

### -param opacityMaskBrush [in]

A pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush">IXpsOMBrush</a> interface to be set as the local, unshared opacity mask brush. A <b>NULL</b> pointer clears the previously assigned opacity mask brush.

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
<i>opacityMaskBrush</i> does not point to a recognized interface implementation. Custom implementation of XPS Document API interfaces is not supported.

</td>
</tr>
</table>

## -remarks

After you call <b>SetOpacityMaskBrushLocal</b>, the opacity mask brush lookup key is released and <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisual-getopacitymaskbrushlookup">GetOpacityMaskBrushLookup</a> returns a <b>NULL</b> pointer in the <i>key</i> parameter. The table that follows explains the relationship between the local and lookup values of this property.


<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned in <i>opacityMaskBrush</i> by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisual-getopacitymaskbrush">GetOpacityMaskBrush</a>
</th>
<th>Object that is returned in <i>opacityMaskBrush</i> by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisual-getopacitymaskbrushlocal">GetOpacityMaskBrushLocal</a>
</th>
<th>String that is returned in <i>key</i> by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisual-getopacitymaskbrushlookup">GetOpacityMaskBrushLookup</a>
</th>
</tr>
<tr>
<td>
<b>SetOpacityMaskBrushLocal</b> (this method)

</td>
<td>
The local opacity mask brush that is set by <b>SetOpacityMaskBrushLocal</b>.

</td>
<td>
The local opacity mask brush that is set by <b>SetOpacityMaskBrushLocal</b>.

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
The shared opacity mask brush that gets retrieved, with a lookup key that matches the key that is set by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisual-setopacitymaskbrushlookup">SetOpacityMaskBrushLookup</a>, from the resource directory.

</td>
<td>
<b>NULL</b> pointer.

</td>
<td>
The lookup key that is set by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisual-setopacitymaskbrushlookup">SetOpacityMaskBrushLookup</a>.

</td>
</tr>
<tr>
<td>
Neither <b>SetOpacityMaskBrushLocal</b> nor <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisual-setopacitymaskbrushlookup">SetOpacityMaskBrushLookup</a> has been called yet.

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



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual">IXpsOMVisual</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>