---
UID: NF:xpsobjectmodel.IXpsOMGeometry.GetTransformLocal
title: IXpsOMGeometry::GetTransformLocal (xpsobjectmodel.h)
description: Gets a pointer to the IXpsOMMatrixTransform interface that contains the local, unshared matrix transform for the geometry.
helpviewer_keywords: ["GetTransformLocal","GetTransformLocal method [XPS Documents and Packaging]","GetTransformLocal method [XPS Documents and Packaging]","IXpsOMGeometry interface","IXpsOMGeometry interface [XPS Documents and Packaging]","GetTransformLocal method","IXpsOMGeometry.GetTransformLocal","IXpsOMGeometry::GetTransformLocal","xps.ixpsomgeometry_gettransformlocal","xpsobjectmodel/IXpsOMGeometry::GetTransformLocal"]
old-location: xps\ixpsomgeometry_gettransformlocal.htm
tech.root: xps
ms.assetid: 1ae895a1-7b63-460c-b066-d8e9c7cd03c2
ms.date: 12/05/2018
ms.keywords: GetTransformLocal, GetTransformLocal method [XPS Documents and Packaging], GetTransformLocal method [XPS Documents and Packaging],IXpsOMGeometry interface, IXpsOMGeometry interface [XPS Documents and Packaging],GetTransformLocal method, IXpsOMGeometry.GetTransformLocal, IXpsOMGeometry::GetTransformLocal, xps.ixpsomgeometry_gettransformlocal, xpsobjectmodel/IXpsOMGeometry::GetTransformLocal
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
 - IXpsOMGeometry::GetTransformLocal
 - xpsobjectmodel/IXpsOMGeometry::GetTransformLocal
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
 - IXpsOMGeometry.GetTransformLocal
---

# IXpsOMGeometry::GetTransformLocal


## -description

Gets a pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform">IXpsOMMatrixTransform</a> interface that contains the local, unshared matrix transform for the geometry.

## -parameters

### -param transform [out, retval]

A pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform">IXpsOMMatrixTransform</a> interface that contains the local, unshared matrix transform for the geometry. A <b>NULL</b> pointer is returned if  a local matrix transform has not been set or a matrix transform lookup key has been set.

The value that is returned in this parameter depends on which method has most recently been called to set the transform.

<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned in <i>transform</i></th>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometry-settransformlocal">SetTransformLocal</a>


</td>
<td>
The local transform that is set by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometry-settransformlocal">SetTransformLocal</a>.

</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometry-settransformlookup">SetTransformLookup</a>


</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
<tr>
<td>
Neither <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometry-settransformlocal">SetTransformLocal</a> nor <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometry-settransformlookup">SetTransformLookup</a> has been called yet.

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
<i>transform</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry">IXpsOMGeometry</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>