---
UID: NF:xpsobjectmodel.IXpsOMVisual.GetClipGeometryLocal
title: IXpsOMVisual::GetClipGeometryLocal (xpsobjectmodel.h)
description: Gets a pointer to the IXpsOMGeometry interface that contains the local, unshared geometry of the visual's clipping region.
helpviewer_keywords: ["GetClipGeometryLocal","GetClipGeometryLocal method [XPS Documents and Packaging]","GetClipGeometryLocal method [XPS Documents and Packaging]","IXpsOMVisual interface","IXpsOMVisual interface [XPS Documents and Packaging]","GetClipGeometryLocal method","IXpsOMVisual.GetClipGeometryLocal","IXpsOMVisual::GetClipGeometryLocal","xps.ixpsomvisual_getclipgeometrylocal","xpsobjectmodel/IXpsOMVisual::GetClipGeometryLocal"]
old-location: xps\ixpsomvisual_getclipgeometrylocal.htm
tech.root: xps
ms.assetid: 19efe0d7-6b11-41bc-80e7-e43e64d977b4
ms.date: 12/05/2018
ms.keywords: GetClipGeometryLocal, GetClipGeometryLocal method [XPS Documents and Packaging], GetClipGeometryLocal method [XPS Documents and Packaging],IXpsOMVisual interface, IXpsOMVisual interface [XPS Documents and Packaging],GetClipGeometryLocal method, IXpsOMVisual.GetClipGeometryLocal, IXpsOMVisual::GetClipGeometryLocal, xps.ixpsomvisual_getclipgeometrylocal, xpsobjectmodel/IXpsOMVisual::GetClipGeometryLocal
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
 - IXpsOMVisual::GetClipGeometryLocal
 - xpsobjectmodel/IXpsOMVisual::GetClipGeometryLocal
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
 - IXpsOMVisual.GetClipGeometryLocal
---

# IXpsOMVisual::GetClipGeometryLocal


## -description

Gets a pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry">IXpsOMGeometry</a> interface that contains the local, unshared geometry of the visual's clipping region.

## -parameters

### -param clipGeometry [out, retval]

A pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry">IXpsOMGeometry</a> interface that contains the local, unshared geometry of the visual's clipping region. If a clip geometry lookup key has been set, or if a local clip geometry has not been set, a <b>NULL</b> pointer is returned.

<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned in <i>clipGeometry</i></th>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisual-setclipgeometrylocal">SetClipGeometryLocal</a>


</td>
<td>
The local clip geometry that is set by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisual-setclipgeometrylocal">SetClipGeometryLocal</a>.

</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisual-setclipgeometrylookup">SetClipGeometryLookup</a>


</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
<tr>
<td>
Neither <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisual-setclipgeometrylocal">SetClipGeometryLocal</a> nor <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisual-setclipgeometrylookup">SetClipGeometryLookup</a> has been called yet.

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
<i>clipGeometry</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry">IXpsOMGeometry</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual">IXpsOMVisual</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>