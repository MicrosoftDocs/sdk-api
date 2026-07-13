---
UID: NF:xpsobjectmodel.IXpsOMGeometryFigure.Clone
title: IXpsOMGeometryFigure::Clone (xpsobjectmodel.h)
description: Makes a deep copy of the interface. (IXpsOMGeometryFigure.Clone)
helpviewer_keywords: ["Clone","Clone method [XPS Documents and Packaging]","Clone method [XPS Documents and Packaging]","IXpsOMGeometryFigure interface","IXpsOMGeometryFigure interface [XPS Documents and Packaging]","Clone method","IXpsOMGeometryFigure.Clone","IXpsOMGeometryFigure::Clone","xps.ixpsomgeometryfigure_clone","xpsobjectmodel/IXpsOMGeometryFigure::Clone"]
old-location: xps\ixpsomgeometryfigure_clone.htm
tech.root: xps
ms.assetid: 97876b95-7b68-4c91-ab15-0708bad3876f
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [XPS Documents and Packaging], Clone method [XPS Documents and Packaging],IXpsOMGeometryFigure interface, IXpsOMGeometryFigure interface [XPS Documents and Packaging],Clone method, IXpsOMGeometryFigure.Clone, IXpsOMGeometryFigure::Clone, xps.ixpsomgeometryfigure_clone, xpsobjectmodel/IXpsOMGeometryFigure::Clone
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
 - IXpsOMGeometryFigure::Clone
 - xpsobjectmodel/IXpsOMGeometryFigure::Clone
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
 - IXpsOMGeometryFigure.Clone
---

# IXpsOMGeometryFigure::Clone


## -description

Makes a deep copy of the interface.

## -parameters

### -param geometryFigure [out, retval]

A pointer to the copy of the interface.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

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
<i>geometryFigure</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The owner of the copy is <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure">IXpsOMGeometryFigure</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>
