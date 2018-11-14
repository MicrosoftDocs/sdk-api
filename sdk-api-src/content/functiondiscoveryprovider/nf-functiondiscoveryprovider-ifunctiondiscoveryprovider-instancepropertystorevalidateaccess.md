---
UID: NF:functiondiscoveryprovider.IFunctionDiscoveryProvider.InstancePropertyStoreValidateAccess
title: IFunctionDiscoveryProvider::InstancePropertyStoreValidateAccess
author: windows-sdk-content
description: Verifies that the provider supports the requested access.
old-location: ncd\ifunctiondiscoveryprovider_instancepropertystorevalidateaccess.htm
tech.root: fundisc
ms.assetid: 0ee8d65d-0be3-4171-946a-10a15b8f8eb7
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IFunctionDiscoveryProvider interface,InstancePropertyStoreValidateAccess method, IFunctionDiscoveryProvider.InstancePropertyStoreValidateAccess, IFunctionDiscoveryProvider::InstancePropertyStoreValidateAccess, InstancePropertyStoreValidateAccess, InstancePropertyStoreValidateAccess method, InstancePropertyStoreValidateAccess method,IFunctionDiscoveryProvider interface, STGM_READ, STGM_READWRITE, STGM_WRITE, functiondiscoveryprovider/IFunctionDiscoveryProvider::InstancePropertyStoreValidateAccess, ncd.ifunctiondiscoveryprovider_instancepropertystorevalidateaccess
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
 - IFunctionDiscoveryProvider.InstancePropertyStoreValidateAccess
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
- IFunctionDiscoveryProvider.InstancePropertyStoreValidateAccess
: 
---

# IFunctionDiscoveryProvider::InstancePropertyStoreValidateAccess


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Verifies that the provider supports the  requested access. It is called when <a href="https://msdn.microsoft.com/3e03567b-7bac-4bef-ae62-a040f0c33cfb">OpenPropertyStore</a> is called on a function instance to verify that the provider supports the access mode passed by the <i>dwStgAccess</i> parameter.   

This method is only called when a provider's <a href="https://msdn.microsoft.com/084d6d91-4637-4325-887b-e9f46ecaaee4">Initialize</a> method returns  a <i>pdwStgAccessCapabilities</i> parameter value of -1. 


## -parameters




### -param pIFunctionInstance [in]

A pointer to the <a href="https://msdn.microsoft.com/cc421719-73a6-4d4d-9bf8-171e46c4e275">IFunctionInstance</a> interface.


### -param iProviderInstanceContext [in]

The context associated with the specific function instance.


### -param dwStgAccess [in]

The access mode to be verified.  For this method, the following modes are supported: 

<a id="STGM_READ"></a>
<a id="stgm_read"></a>


#### STGM_READ

<a id="STGM_READWRITE"></a>
<a id="stgm_readwrite"></a>


#### STGM_READWRITE

<a id="STGM_WRITE"></a>
<a id="stgm_write"></a>


#### STGM_WRITE


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
The value of <i>dwStgAccess</i> is invalid.

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



The precise meaning of the STG_E_ACCESSDENIED return value is implementation-specific. When you implement the <b>InstancePropertyStoreValidateAccess</b> method, you can return STG_E_ACCESSDENIED for any supplied <i>dwStgAccess</i> mode value on any supplied function instance. 




## -see-also




<a href="https://msdn.microsoft.com/e0019d0d-1495-4a0e-a7d9-7772046a4a26">IFunctionDiscoveryProvider</a>
 

 

