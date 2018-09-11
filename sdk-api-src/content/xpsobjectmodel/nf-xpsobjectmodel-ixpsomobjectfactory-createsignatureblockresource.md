---
UID: NF:xpsobjectmodel.IXpsOMObjectFactory.CreateSignatureBlockResource
title: IXpsOMObjectFactory::CreateSignatureBlockResource
author: windows-sdk-content
description: Creates an IXpsOMSignatureBlockResource that can contain one or more signature requests.
old-location: xps\ixpsomobjectfactory_createsignatureblockresource.htm
tech.root: printdocs
ms.assetid: 0948d495-f2da-4361-8365-d4316da72524
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CreateSignatureBlockResource, CreateSignatureBlockResource method [XPS Documents and Packaging], CreateSignatureBlockResource method [XPS Documents and Packaging],IXpsOMObjectFactory interface, IXpsOMObjectFactory interface [XPS Documents and Packaging],CreateSignatureBlockResource method, IXpsOMObjectFactory.CreateSignatureBlockResource, IXpsOMObjectFactory::CreateSignatureBlockResource, xps.ixpsomobjectfactory_createsignatureblockresource, xpsobjectmodel/IXpsOMObjectFactory::CreateSignatureBlockResource
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMObjectFactory.CreateSignatureBlockResource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMObjectFactory::CreateSignatureBlockResource


## -description


Creates an <a href="https://msdn.microsoft.com/f5052470-487d-4f47-8d42-70538a4a45a8">IXpsOMSignatureBlockResource</a> that can contain one or more signature requests.


## -parameters




### -param acquiredStream [in]

A read-only stream to be associated with this resource.


### -param partUri [in]

A pointer to the <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface that contains the part name to be  assigned to this resource.


### -param signatureBlockResource [out, retval]

A pointer to the new <a href="https://msdn.microsoft.com/f5052470-487d-4f47-8d42-70538a4a45a8">IXpsOMSignatureBlockResource</a> interface created by this method.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>.

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




<a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a>



<a href="https://msdn.microsoft.com/2444703e-4b89-4ef0-9ed7-aa937bc62e8c">IXpsOMObjectFactory</a>



<a href="https://msdn.microsoft.com/f5052470-487d-4f47-8d42-70538a4a45a8">IXpsOMSignatureBlockResource</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

