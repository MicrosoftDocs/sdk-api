---
UID: NF:functiondiscoveryprovider.IFunctionDiscoveryProvider.InstancePropertyStoreFlush
title: IFunctionDiscoveryProvider::InstancePropertyStoreFlush
author: windows-sdk-content
description: Provides a mechanism for the provider to persist properties.
old-location: ncd\ifunctiondiscoveryprovider_instancepropertystoreflush.htm
tech.root: fundisc
ms.assetid: 7ad29f46-fb21-4287-9fc9-9ab86d44d298
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IFunctionDiscoveryProvider interface,InstancePropertyStoreFlush method, IFunctionDiscoveryProvider.InstancePropertyStoreFlush, IFunctionDiscoveryProvider::InstancePropertyStoreFlush, InstancePropertyStoreFlush, InstancePropertyStoreFlush method, InstancePropertyStoreFlush method,IFunctionDiscoveryProvider interface, functiondiscoveryprovider/IFunctionDiscoveryProvider::InstancePropertyStoreFlush, ncd.ifunctiondiscoveryprovider_instancepropertystoreflush
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IFunctionDiscoveryProvider.InstancePropertyStoreFlush
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- functiondiscoveryprovider.h
: 
- IFunctionDiscoveryProvider.InstancePropertyStoreFlush
: 
---

# IFunctionDiscoveryProvider::InstancePropertyStoreFlush


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Provides a mechanism for the provider to persist properties without having to implement <a href="https://msdn.microsoft.com/d6d3d1d1-d2fb-409c-be37-3cd286e325a3">IProviderProperties</a>. This method is called whenever <a href="https://msdn.microsoft.com/en-us/library/Ff536957(v=VS.85).aspx">IPropertyStore::Commit</a> is called by the client on the function instance property store.


## -parameters




### -param pIFunctionInstance [in]

 A pointer to the <a href="https://msdn.microsoft.com/cc421719-73a6-4d4d-9bf8-171e46c4e275">IFunctionInstance</a> interface.


### -param iProviderInstanceContext [in]

The context associated with the specific function instance.


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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The provider does not implement an instance property store.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters contains an invalid argument.

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



If the provider keeps the new values that are passed through <a href="https://msdn.microsoft.com/5aa3e6a3-febc-4d2d-b58b-abfad28d325d">SetValue</a> cached in memory, this method should implement the code to persist the updated values to the underlying API/store.

If you implement this method, you should call <a href="https://msdn.microsoft.com/3e03567b-7bac-4bef-ae62-a040f0c33cfb">OpenPropertyStore</a> to return the current property store before persisting the data.




## -see-also




<a href="https://msdn.microsoft.com/e0019d0d-1495-4a0e-a7d9-7772046a4a26">IFunctionDiscoveryProvider</a>
 

 

