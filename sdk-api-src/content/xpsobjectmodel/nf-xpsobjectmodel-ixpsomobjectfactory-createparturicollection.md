---
UID: NF:xpsobjectmodel.IXpsOMObjectFactory.CreatePartUriCollection
title: IXpsOMObjectFactory::CreatePartUriCollection (xpsobjectmodel.h)
description: Creates an IXpsOMPartUriCollection interface that can contain IOpcPartUri interface pointers.
helpviewer_keywords: ["CreatePartUriCollection","CreatePartUriCollection method [XPS Documents and Packaging]","CreatePartUriCollection method [XPS Documents and Packaging]","IXpsOMObjectFactory interface","IXpsOMObjectFactory interface [XPS Documents and Packaging]","CreatePartUriCollection method","IXpsOMObjectFactory.CreatePartUriCollection","IXpsOMObjectFactory::CreatePartUriCollection","xps.ixpsomobjectfactory_createparturicollection","xpsobjectmodel/IXpsOMObjectFactory::CreatePartUriCollection"]
old-location: xps\ixpsomobjectfactory_createparturicollection.htm
tech.root: xps
ms.assetid: 1127a314-43c8-43a2-a06e-88858a43c519
ms.date: 12/05/2018
ms.keywords: CreatePartUriCollection, CreatePartUriCollection method [XPS Documents and Packaging], CreatePartUriCollection method [XPS Documents and Packaging],IXpsOMObjectFactory interface, IXpsOMObjectFactory interface [XPS Documents and Packaging],CreatePartUriCollection method, IXpsOMObjectFactory.CreatePartUriCollection, IXpsOMObjectFactory::CreatePartUriCollection, xps.ixpsomobjectfactory_createparturicollection, xpsobjectmodel/IXpsOMObjectFactory::CreatePartUriCollection
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
 - IXpsOMObjectFactory::CreatePartUriCollection
 - xpsobjectmodel/IXpsOMObjectFactory::CreatePartUriCollection
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
 - IXpsOMObjectFactory.CreatePartUriCollection
---

# IXpsOMObjectFactory::CreatePartUriCollection


## -description

Creates an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomparturicollection">IXpsOMPartUriCollection</a> interface that can contain <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface pointers.

## -parameters

### -param partUriCollection [out, retval]

A pointer to the new <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomparturicollection">IXpsOMPartUriCollection</a> interface.

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
<i>partUriCollection</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory">IXpsOMObjectFactory</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomparturicollection">IXpsOMPartUriCollection</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>