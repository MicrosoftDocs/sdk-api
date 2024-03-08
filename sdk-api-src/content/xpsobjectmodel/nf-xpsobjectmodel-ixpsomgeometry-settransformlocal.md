---
UID: NF:xpsobjectmodel.IXpsOMGeometry.SetTransformLocal
title: IXpsOMGeometry::SetTransformLocal (xpsobjectmodel.h)
description: Sets the local, unshared matrix transform. (IXpsOMGeometry.SetTransformLocal)
helpviewer_keywords: ["IXpsOMGeometry interface [XPS Documents and Packaging]","SetTransformLocal method","IXpsOMGeometry.SetTransformLocal","IXpsOMGeometry::SetTransformLocal","SetTransformLocal","SetTransformLocal method [XPS Documents and Packaging]","SetTransformLocal method [XPS Documents and Packaging]","IXpsOMGeometry interface","xps.ixpsomgeometry_settransformlocal","xpsobjectmodel/IXpsOMGeometry::SetTransformLocal"]
old-location: xps\ixpsomgeometry_settransformlocal.htm
tech.root: xps
ms.assetid: ca4a458d-e2e5-4f8c-aac1-35f5ff91a0d9
ms.date: 12/05/2018
ms.keywords: IXpsOMGeometry interface [XPS Documents and Packaging],SetTransformLocal method, IXpsOMGeometry.SetTransformLocal, IXpsOMGeometry::SetTransformLocal, SetTransformLocal, SetTransformLocal method [XPS Documents and Packaging], SetTransformLocal method [XPS Documents and Packaging],IXpsOMGeometry interface, xps.ixpsomgeometry_settransformlocal, xpsobjectmodel/IXpsOMGeometry::SetTransformLocal
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
 - IXpsOMGeometry::SetTransformLocal
 - xpsobjectmodel/IXpsOMGeometry::SetTransformLocal
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
 - IXpsOMGeometry.SetTransformLocal
---

# IXpsOMGeometry::SetTransformLocal


## -description

Sets the local, unshared matrix transform.

## -parameters

### -param transform [in]

A pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform">IXpsOMMatrixTransform</a> interface to be set as the local, unshared matrix transform for the geometry.

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
<i>transform</i> does not point to a recognized interface implementation. Custom implementation of XPS Document API interfaces is not supported.

</td>
</tr>
</table>

## -remarks

After you call <b>SetTransformLocal</b>, the transform lookup key is released and <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometry-gettransformlookup">GetTransformLookup</a> returns a <b>NULL</b> pointer in the <i>lookup</i> parameter. The table that follows explains the relationship between the local and lookup values of this property.

<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned in <i>transform</i> by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometry-gettransform">GetTransform</a>
</th>
<th>Object that is returned in <i>transform</i> by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometry-gettransformlocal">GetTransformLocal</a>
</th>
<th>Object that is returned in <i>lookup</i> by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometry-gettransformlookup">GetTransformLookup</a>
</th>
</tr>
<tr>
<td>
<b>SetTransformLocal</b> (this method)

</td>
<td>
The local transform that is set by <b>SetTransformLocal</b>.

</td>
<td>
The local transform that is set by <b>SetTransformLocal</b>.

</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometry-settransformlookup">SetTransformLookup</a>


</td>
<td>
The shared transform retrieved, with a lookup key that matches the key that is set by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometry-settransformlookup">SetTransformLookup</a>, from the resource directory.

</td>
<td>
<b>NULL</b> pointer.

</td>
<td>
The lookup key that is set by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometry-settransformlookup">SetTransformLookup</a>.

</td>
</tr>
<tr>
<td>
Neither <b>SetTransformLocal</b> nor <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometry-settransformlookup">SetTransformLookup</a> has been called yet.

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

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry">IXpsOMGeometry</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>
