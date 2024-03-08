---
UID: NF:xpsobjectmodel.IXpsOMGeometry.Clone
title: IXpsOMGeometry::Clone (xpsobjectmodel.h)
description: Makes a deep copy of the interface. (IXpsOMGeometry.Clone)
helpviewer_keywords: ["Clone","Clone method [XPS Documents and Packaging]","Clone method [XPS Documents and Packaging]","IXpsOMGeometry interface","IXpsOMGeometry interface [XPS Documents and Packaging]","Clone method","IXpsOMGeometry.Clone","IXpsOMGeometry::Clone","xps.ixpsomgeometry_clone","xpsobjectmodel/IXpsOMGeometry::Clone"]
old-location: xps\ixpsomgeometry_clone.htm
tech.root: xps
ms.assetid: 79f48f2e-884f-4afd-8f08-3285faf6c217
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [XPS Documents and Packaging], Clone method [XPS Documents and Packaging],IXpsOMGeometry interface, IXpsOMGeometry interface [XPS Documents and Packaging],Clone method, IXpsOMGeometry.Clone, IXpsOMGeometry::Clone, xps.ixpsomgeometry_clone, xpsobjectmodel/IXpsOMGeometry::Clone
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
 - IXpsOMGeometry::Clone
 - xpsobjectmodel/IXpsOMGeometry::Clone
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
 - IXpsOMGeometry.Clone
---

# IXpsOMGeometry::Clone


## -description

Makes a deep copy of the interface.

## -parameters

### -param geometry [out, retval]

A pointer to the copy of the interface.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory to perform this operation.

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



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>
