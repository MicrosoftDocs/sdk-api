---
UID: NF:xpsobjectmodel.IXpsOMCanvas.Clone
title: IXpsOMCanvas::Clone (xpsobjectmodel.h)
description: Makes a deep copy of the interface. (IXpsOMCanvas.Clone)
helpviewer_keywords: ["Clone","Clone method [XPS Documents and Packaging]","Clone method [XPS Documents and Packaging]","IXpsOMCanvas interface","IXpsOMCanvas interface [XPS Documents and Packaging]","Clone method","IXpsOMCanvas.Clone","IXpsOMCanvas::Clone","xps.ixpsomcanvas_clone","xpsobjectmodel/IXpsOMCanvas::Clone"]
old-location: xps\ixpsomcanvas_clone.htm
tech.root: xps
ms.assetid: 2411fca6-2d36-4704-83a6-0086c6be0e2a
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [XPS Documents and Packaging], Clone method [XPS Documents and Packaging],IXpsOMCanvas interface, IXpsOMCanvas interface [XPS Documents and Packaging],Clone method, IXpsOMCanvas.Clone, IXpsOMCanvas::Clone, xps.ixpsomcanvas_clone, xpsobjectmodel/IXpsOMCanvas::Clone
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
 - IXpsOMCanvas::Clone
 - xpsobjectmodel/IXpsOMCanvas::Clone
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
 - IXpsOMCanvas.Clone
---

# IXpsOMCanvas::Clone


## -description

Makes a deep copy of the interface.

## -parameters

### -param canvas [out, retval]

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
<i>canvas</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The owner of the new interface is <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas">IXpsOMCanvas</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>
