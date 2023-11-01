---
UID: NF:xpsobjectmodel.IXpsOMVisualBrush.Clone
title: IXpsOMVisualBrush::Clone (xpsobjectmodel.h)
description: Makes a deep copy of the interface. (IXpsOMVisualBrush.Clone)
helpviewer_keywords: ["Clone","Clone method [XPS Documents and Packaging]","Clone method [XPS Documents and Packaging]","IXpsOMVisualBrush interface","IXpsOMVisualBrush interface [XPS Documents and Packaging]","Clone method","IXpsOMVisualBrush.Clone","IXpsOMVisualBrush::Clone","xps.ixpsomvisualbrush_clone","xpsobjectmodel/IXpsOMVisualBrush::Clone"]
old-location: xps\ixpsomvisualbrush_clone.htm
tech.root: xps
ms.assetid: c3341566-6b35-4ed9-9db8-d5493656755e
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [XPS Documents and Packaging], Clone method [XPS Documents and Packaging],IXpsOMVisualBrush interface, IXpsOMVisualBrush interface [XPS Documents and Packaging],Clone method, IXpsOMVisualBrush.Clone, IXpsOMVisualBrush::Clone, xps.ixpsomvisualbrush_clone, xpsobjectmodel/IXpsOMVisualBrush::Clone
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
 - IXpsOMVisualBrush::Clone
 - xpsobjectmodel/IXpsOMVisualBrush::Clone
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
 - IXpsOMVisualBrush.Clone
---

# IXpsOMVisualBrush::Clone


## -description

Makes a deep copy of the interface.

## -parameters

### -param visualBrush [out, retval]

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
<i>visualBrush</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

This method does not update the resource pointers in the new <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush">IXpsOMVisualBrush</a>  interface.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush">IXpsOMVisualBrush</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>
