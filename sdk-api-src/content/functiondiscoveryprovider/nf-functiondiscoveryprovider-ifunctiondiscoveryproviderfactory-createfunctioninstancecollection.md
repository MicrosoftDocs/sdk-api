---
UID: NF:functiondiscoveryprovider.IFunctionDiscoveryProviderFactory.CreateFunctionInstanceCollection
title: IFunctionDiscoveryProviderFactory::CreateFunctionInstanceCollection
author: windows-sdk-content
description: Creates a function instance collection.
old-location: ncd\ifunctiondiscoveryproviderfactory_createfunctioninstancecollection.htm
tech.root: FunDisc
ms.assetid: c49f6be1-1789-4415-8898-ad74e0148c47
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateFunctionInstanceCollection, CreateFunctionInstanceCollection method, CreateFunctionInstanceCollection method,IFunctionDiscoveryProviderFactory interface, IFunctionDiscoveryProviderFactory interface,CreateFunctionInstanceCollection method, IFunctionDiscoveryProviderFactory.CreateFunctionInstanceCollection, IFunctionDiscoveryProviderFactory::CreateFunctionInstanceCollection, functiondiscoveryprovider/IFunctionDiscoveryProviderFactory::CreateFunctionInstanceCollection, ncd.ifunctiondiscoveryproviderfactory_createfunctioninstancecollection
ms.topic: method
req.header: functiondiscoveryprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FunctionDiscoveryProvider.idl
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
 - FunctionDiscoveryProvider.h
api_name:
 - IFunctionDiscoveryProviderFactory.CreateFunctionInstanceCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFunctionDiscoveryProviderFactory::CreateFunctionInstanceCollection


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Creates a function instance collection.


## -parameters




### -param ppIFunctionInstanceCollection [out]

A pointer to an <a href="https://msdn.microsoft.com/8ac1a406-92f3-4e39-985e-ab8fa7d28751">IFunctionInstanceCollection</a> interface pointer.


## -returns



This method can return one of these values.


Possible return values include, but are not limited to, the following.



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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The value of <i>ppIFunctionInstanceCollection</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method is unable to allocate the memory required to perform this operation.

</td>
</tr>
</table>
 




## -remarks



Providers that return results synchronously through the <i>ppIFunctionInstanceCollection</i> parameter of the <a href="https://msdn.microsoft.com/8c368ea7-c9db-4e80-a080-eef8068f7402">IFunctionDiscoveryProvider::Query</a> method can use this to create a collection to return the results with.


Client programmers can create and use the Function Discovery instance collection object, as it can also be created using <b>CoCreateInstance</b>.





## -see-also




<a href="https://msdn.microsoft.com/576db617-0bca-4b46-839b-0f133f28cacb">IFunctionDiscoveryProviderFactory</a>
 

 

