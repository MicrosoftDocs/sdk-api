---
UID: NF:xpsobjectmodel.IXpsOMPath.GetGeometryLocal
title: IXpsOMPath::GetGeometryLocal (xpsobjectmodel.h)
description: Gets the local, unshared geometry of the resolved fill area for this path.
helpviewer_keywords: ["GetGeometryLocal","GetGeometryLocal method [XPS Documents and Packaging]","GetGeometryLocal method [XPS Documents and Packaging]","IXpsOMPath interface","IXpsOMPath interface [XPS Documents and Packaging]","GetGeometryLocal method","IXpsOMPath.GetGeometryLocal","IXpsOMPath::GetGeometryLocal","xps.ixpsompath_getgeometrylocal","xpsobjectmodel/IXpsOMPath::GetGeometryLocal"]
old-location: xps\ixpsompath_getgeometrylocal.htm
tech.root: xps
ms.assetid: a8902191-7646-4c97-843f-9467ed12f621
ms.date: 12/05/2018
ms.keywords: GetGeometryLocal, GetGeometryLocal method [XPS Documents and Packaging], GetGeometryLocal method [XPS Documents and Packaging],IXpsOMPath interface, IXpsOMPath interface [XPS Documents and Packaging],GetGeometryLocal method, IXpsOMPath.GetGeometryLocal, IXpsOMPath::GetGeometryLocal, xps.ixpsompath_getgeometrylocal, xpsobjectmodel/IXpsOMPath::GetGeometryLocal
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
 - IXpsOMPath::GetGeometryLocal
 - xpsobjectmodel/IXpsOMPath::GetGeometryLocal
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
 - IXpsOMPath.GetGeometryLocal
---

# IXpsOMPath::GetGeometryLocal


## -description

Gets the local, unshared geometry of the  resolved fill area for this path.

## -parameters

### -param geometry [out, retval]

The local, unshared geometry of the  resolved fill area for this path. If a geometry lookup key has been set or if a local geometry has not been set, a <b>NULL</b> pointer is returned.

<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned in <i>geometry</i></th>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setgeometrylocal">SetGeometryLocal</a>


</td>
<td>
The local geometry that is set by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setgeometrylocal">SetGeometryLocal</a>.

</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setgeometrylookup">SetGeometryLookup</a>


</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
<tr>
<td>
Neither <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setgeometrylocal">SetGeometryLocal</a> nor <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setgeometrylookup">SetGeometryLookup</a> has been called yet.

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
<i>geometry</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry">IXpsOMGeometry</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath">IXpsOMPath</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>