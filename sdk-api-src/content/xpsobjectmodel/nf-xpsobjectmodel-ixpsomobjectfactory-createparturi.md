---
UID: NF:xpsobjectmodel.IXpsOMObjectFactory.CreatePartUri
title: IXpsOMObjectFactory::CreatePartUri (xpsobjectmodel.h)
author: windows-sdk-content
description: Creates an IOpcPartUri interface that uses the specified URI.
old-location: xps\ixpsomobjectfactory_createparturi.htm
tech.root: printdocs
ms.assetid: 0ed86fd1-ebc0-4eb6-a332-0dea3a21c100
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreatePartUri, CreatePartUri method [XPS Documents and Packaging], CreatePartUri method [XPS Documents and Packaging],IXpsOMObjectFactory interface, IXpsOMObjectFactory interface [XPS Documents and Packaging],CreatePartUri method, IXpsOMObjectFactory.CreatePartUri, IXpsOMObjectFactory::CreatePartUri, xps.ixpsomobjectfactory_createparturi, xpsobjectmodel/IXpsOMObjectFactory::CreatePartUri
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
 - IXpsOMObjectFactory.CreatePartUri
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMObjectFactory::CreatePartUri


## -description


Creates an <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface that uses the specified URI.


## -parameters




### -param uri [in]

The URI string.


### -param partUri [out, retval]

A pointer to the <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface created by this method.


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
<i>partUri</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a>



<a href="https://msdn.microsoft.com/2444703e-4b89-4ef0-9ed7-aa937bc62e8c">IXpsOMObjectFactory</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

