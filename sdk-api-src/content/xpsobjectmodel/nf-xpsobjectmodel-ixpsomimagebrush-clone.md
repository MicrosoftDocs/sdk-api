---
UID: NF:xpsobjectmodel.IXpsOMImageBrush.Clone
title: IXpsOMImageBrush::Clone (xpsobjectmodel.h)
description: Makes a deep copy of the interface. (IXpsOMImageBrush.Clone)
helpviewer_keywords: ["Clone","Clone method [XPS Documents and Packaging]","Clone method [XPS Documents and Packaging]","IXpsOMImageBrush interface","IXpsOMImageBrush interface [XPS Documents and Packaging]","Clone method","IXpsOMImageBrush.Clone","IXpsOMImageBrush::Clone","xps.ixpsomimagebrush_clone","xpsobjectmodel/IXpsOMImageBrush::Clone"]
old-location: xps\ixpsomimagebrush_clone.htm
tech.root: xps
ms.assetid: 7c10f6e5-b223-4ddb-9fcf-c9f7bf82953f
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [XPS Documents and Packaging], Clone method [XPS Documents and Packaging],IXpsOMImageBrush interface, IXpsOMImageBrush interface [XPS Documents and Packaging],Clone method, IXpsOMImageBrush.Clone, IXpsOMImageBrush::Clone, xps.ixpsomimagebrush_clone, xpsobjectmodel/IXpsOMImageBrush::Clone
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
 - IXpsOMImageBrush::Clone
 - xpsobjectmodel/IXpsOMImageBrush::Clone
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
 - IXpsOMImageBrush.Clone
---

# IXpsOMImageBrush::Clone


## -description

Makes a deep copy of the interface.

## -parameters

### -param imageBrush [out, retval]

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
<i>imageBrush</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

This method does not update any of the resource pointers in the copy.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush">IXpsOMImageBrush</a>



<a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>
