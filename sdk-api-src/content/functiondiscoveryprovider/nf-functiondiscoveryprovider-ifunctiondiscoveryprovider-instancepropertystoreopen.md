---
UID: NF:functiondiscoveryprovider.IFunctionDiscoveryProvider.InstancePropertyStoreOpen
title: IFunctionDiscoveryProvider::InstancePropertyStoreOpen (functiondiscoveryprovider.h)
author: windows-sdk-content
description: Opens the property store of the provider.
old-location: ncd\ifunctiondiscoveryprovider_instancepropertystoreopen.htm
tech.root: FunDisc
ms.assetid: 35e98e8a-5e6c-4cbb-9a61-9720f11f90d6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFunctionDiscoveryProvider interface,InstancePropertyStoreOpen method, IFunctionDiscoveryProvider.InstancePropertyStoreOpen, IFunctionDiscoveryProvider::InstancePropertyStoreOpen, InstancePropertyStoreOpen, InstancePropertyStoreOpen method, InstancePropertyStoreOpen method,IFunctionDiscoveryProvider interface, STGM_READ, STGM_READWRITE, STGM_WRITE, functiondiscoveryprovider/IFunctionDiscoveryProvider::InstancePropertyStoreOpen, ncd.ifunctiondiscoveryprovider_instancepropertystoreopen
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
 - IFunctionDiscoveryProvider.InstancePropertyStoreOpen
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFunctionDiscoveryProvider::InstancePropertyStoreOpen


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Opens the property store of the provider. This method is called whenever <a href="https://msdn.microsoft.com/3e03567b-7bac-4bef-ae62-a040f0c33cfb">IFunctionInstance::OpenPropertyStore</a> is called if the provider did not provide a property store at creation time.  The provider can provide the property store at this time, or handle the <a href="https://msdn.microsoft.com/d6d3d1d1-d2fb-409c-be37-3cd286e325a3">IProviderProperties</a> methods as they are called.


## -parameters




### -param pIFunctionInstance [in]

A pointer to the <a href="https://msdn.microsoft.com/cc421719-73a6-4d4d-9bf8-171e46c4e275">IFunctionInstance</a> interface for the store that is to be opened. Each property store is associated with a function instance.


### -param iProviderInstanceContext [in]

The context associated with the specific function instance.


### -param dwStgAccess [in]

The access mode to be assigned to the open stream.  For this method, the following modes are supported:

<a id="STGM_READ"></a>
<a id="stgm_read"></a>


#### STGM_READ

<a id="STGM_READWRITE"></a>
<a id="stgm_readwrite"></a>


#### STGM_READWRITE

<a id="STGM_WRITE"></a>
<a id="stgm_write"></a>


#### STGM_WRITE


### -param ppIPropertyStore [out]

A pointer to an <b>IPropertyStore</b> interface pointer.


## -returns



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
<dt><b>STG_E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The method could not open a writeable property store because the caller has insufficient access, the discovery provider does not allow write access to its property store, or another property store is already open for this function instance.

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
 




## -see-also




<a href="https://msdn.microsoft.com/e0019d0d-1495-4a0e-a7d9-7772046a4a26">IFunctionDiscoveryProvider</a>
 

 

