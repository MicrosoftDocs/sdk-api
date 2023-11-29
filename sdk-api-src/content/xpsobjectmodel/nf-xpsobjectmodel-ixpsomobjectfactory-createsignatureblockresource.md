---
UID: NF:xpsobjectmodel.IXpsOMObjectFactory.CreateSignatureBlockResource
title: IXpsOMObjectFactory::CreateSignatureBlockResource (xpsobjectmodel.h)
description: Creates an IXpsOMSignatureBlockResource that can contain one or more signature requests.
helpviewer_keywords: ["CreateSignatureBlockResource","CreateSignatureBlockResource method [XPS Documents and Packaging]","CreateSignatureBlockResource method [XPS Documents and Packaging]","IXpsOMObjectFactory interface","IXpsOMObjectFactory interface [XPS Documents and Packaging]","CreateSignatureBlockResource method","IXpsOMObjectFactory.CreateSignatureBlockResource","IXpsOMObjectFactory::CreateSignatureBlockResource","xps.ixpsomobjectfactory_createsignatureblockresource","xpsobjectmodel/IXpsOMObjectFactory::CreateSignatureBlockResource"]
old-location: xps\ixpsomobjectfactory_createsignatureblockresource.htm
tech.root: xps
ms.assetid: 0948d495-f2da-4361-8365-d4316da72524
ms.date: 12/05/2018
ms.keywords: CreateSignatureBlockResource, CreateSignatureBlockResource method [XPS Documents and Packaging], CreateSignatureBlockResource method [XPS Documents and Packaging],IXpsOMObjectFactory interface, IXpsOMObjectFactory interface [XPS Documents and Packaging],CreateSignatureBlockResource method, IXpsOMObjectFactory.CreateSignatureBlockResource, IXpsOMObjectFactory::CreateSignatureBlockResource, xps.ixpsomobjectfactory_createsignatureblockresource, xpsobjectmodel/IXpsOMObjectFactory::CreateSignatureBlockResource
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
 - IXpsOMObjectFactory::CreateSignatureBlockResource
 - xpsobjectmodel/IXpsOMObjectFactory::CreateSignatureBlockResource
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
 - IXpsOMObjectFactory.CreateSignatureBlockResource
---

# IXpsOMObjectFactory::CreateSignatureBlockResource


## -description

Creates an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsignatureblockresource">IXpsOMSignatureBlockResource</a> that can contain one or more signature requests.

## -parameters

### -param acquiredStream [in]

A read-only stream to be associated with this resource.

### -param partUri [in]

A pointer to the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface that contains the part name to be  assigned to this resource.

### -param signatureBlockResource [out, retval]

A pointer to the new <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsignatureblockresource">IXpsOMSignatureBlockResource</a> interface created by this method.

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
<i>acquiredStream</i>,  <i>partUri</i>, or <i>signatureBlockResource</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory">IXpsOMObjectFactory</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsignatureblockresource">IXpsOMSignatureBlockResource</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>