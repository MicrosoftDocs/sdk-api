---
UID: NF:xpsobjectmodel.IXpsOMObjectFactory.CreateRemoteDictionaryResourceFromStream
title: IXpsOMObjectFactory::CreateRemoteDictionaryResourceFromStream
author: windows-sdk-content
description: Loads the remote resource dictionary markup into an unrooted IXpsOMRemoteDictionaryResource interface.
old-location: xps\ixpsomobjectfactory_createremotedictionaryresourcefromstream.htm
old-project: printdocs
ms.assetid: 996a97f5-320f-4e51-af15-f3b125d4f6c8
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: CreateRemoteDictionaryResourceFromStream, CreateRemoteDictionaryResourceFromStream method [XPS Documents and Packaging], CreateRemoteDictionaryResourceFromStream method [XPS Documents and Packaging],IXpsOMObjectFactory interface, IXpsOMObjectFactory interface [XPS Documents and Packaging],CreateRemoteDictionaryResourceFromStream method, IXpsOMObjectFactory.CreateRemoteDictionaryResourceFromStream, IXpsOMObjectFactory::CreateRemoteDictionaryResourceFromStream, xps.ixpsomobjectfactory_createremotedictionaryresourcefromstream, xpsobjectmodel/IXpsOMObjectFactory::CreateRemoteDictionaryResourceFromStream
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: XPS_INTERLEAVING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMObjectFactory.CreateRemoteDictionaryResourceFromStream
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMObjectFactory::CreateRemoteDictionaryResourceFromStream


## -description


Loads the  remote resource dictionary markup into an unrooted <a href="https://msdn.microsoft.com/dd757856-f16e-46ad-b865-8203c3428372">IXpsOMRemoteDictionaryResource</a> interface.


## -parameters




### -param dictionaryMarkupStream [in]

The <b>IStream</b> interface that contains the remote resource dictionary markup.


### -param dictionaryPartUri [in]

The <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface that contains the part name to be assigned to this resource.


### -param resources [in]

The <a href="https://msdn.microsoft.com/9f706f23-25a0-40ee-93f4-3d7ac98ad6ed">IXpsOMPartResources</a> interface for the part resources of the dictionary resource objects  that have streams.


### -param dictionaryResource [out, retval]

A pointer to the new <a href="https://msdn.microsoft.com/dd757856-f16e-46ad-b865-8203c3428372">IXpsOMRemoteDictionaryResource</a> interface.


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
<i>dictionaryMarkupStream</i>,  <i>dictionaryPartUri</i>, <i>resources</i>, or <i>dictionaryResource</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_NO_CUSTOM_OBJECTS</b></dt>
</dl>
</td>
<td width="60%">
<i>resources</i> does not point to a recognized interface implementation. Custom implementation of XPS Document API interfaces is not supported.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a>



<a href="https://msdn.microsoft.com/2444703e-4b89-4ef0-9ed7-aa937bc62e8c">IXpsOMObjectFactory</a>



<a href="https://msdn.microsoft.com/9f706f23-25a0-40ee-93f4-3d7ac98ad6ed">IXpsOMPartResources</a>



<a href="https://msdn.microsoft.com/dd757856-f16e-46ad-b865-8203c3428372">IXpsOMRemoteDictionaryResource</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

