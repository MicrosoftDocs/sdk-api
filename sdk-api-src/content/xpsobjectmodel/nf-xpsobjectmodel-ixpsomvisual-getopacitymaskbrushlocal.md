---
UID: NF:xpsobjectmodel.IXpsOMVisual.GetOpacityMaskBrushLocal
title: IXpsOMVisual::GetOpacityMaskBrushLocal (xpsobjectmodel.h)
description: Gets the local, unshared opacity mask brush for the visual.
helpviewer_keywords: ["GetOpacityMaskBrushLocal","GetOpacityMaskBrushLocal method [XPS Documents and Packaging]","GetOpacityMaskBrushLocal method [XPS Documents and Packaging]","IXpsOMVisual interface","IXpsOMVisual interface [XPS Documents and Packaging]","GetOpacityMaskBrushLocal method","IXpsOMVisual.GetOpacityMaskBrushLocal","IXpsOMVisual::GetOpacityMaskBrushLocal","xps.ixpsomvisual_getopacitymaskbrushlocal","xpsobjectmodel/IXpsOMVisual::GetOpacityMaskBrushLocal"]
old-location: xps\ixpsomvisual_getopacitymaskbrushlocal.htm
tech.root: xps
ms.assetid: 654dc003-25a6-4186-9c3b-7fe6f82b5481
ms.date: 12/05/2018
ms.keywords: GetOpacityMaskBrushLocal, GetOpacityMaskBrushLocal method [XPS Documents and Packaging], GetOpacityMaskBrushLocal method [XPS Documents and Packaging],IXpsOMVisual interface, IXpsOMVisual interface [XPS Documents and Packaging],GetOpacityMaskBrushLocal method, IXpsOMVisual.GetOpacityMaskBrushLocal, IXpsOMVisual::GetOpacityMaskBrushLocal, xps.ixpsomvisual_getopacitymaskbrushlocal, xpsobjectmodel/IXpsOMVisual::GetOpacityMaskBrushLocal
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
 - IXpsOMVisual::GetOpacityMaskBrushLocal
 - xpsobjectmodel/IXpsOMVisual::GetOpacityMaskBrushLocal
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
 - IXpsOMVisual.GetOpacityMaskBrushLocal
---

# IXpsOMVisual::GetOpacityMaskBrushLocal


## -description

Gets the local, unshared opacity mask brush for the visual.

## -parameters

### -param opacityMaskBrush [out, retval]

A pointer to the  <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush">IXpsOMBrush</a> interface of the visual's opacity mask brush. If an opacity mask brush lookup key has been set, or if a local opacity mask brush has not been set, a <b>NULL</b> pointer is returned.

<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned in <i>opacityMaskBrush</i></th>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisual-setopacitymaskbrushlocal">SetOpacityMaskBrushLocal</a>


</td>
<td>
The local opacity mask brush that is set by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisual-setopacitymaskbrushlocal">SetOpacityMaskBrushLocal</a>.

</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisual-setopacitymaskbrushlookup">SetOpacityMaskBrushLookup</a>


</td>
<td>
<b>NULL</b> pointer.

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
<i>opacityMaskBrush</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush">IXpsOMBrush</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual">IXpsOMVisual</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>