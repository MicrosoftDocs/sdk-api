---
UID: NF:functiondiscoveryprovider.IFunctionDiscoveryProvider.InstancePropertyStoreOpen
title: IFunctionDiscoveryProvider::InstancePropertyStoreOpen (functiondiscoveryprovider.h)
description: Opens the property store of the provider.
helpviewer_keywords: ["IFunctionDiscoveryProvider interface","InstancePropertyStoreOpen method","IFunctionDiscoveryProvider.InstancePropertyStoreOpen","IFunctionDiscoveryProvider::InstancePropertyStoreOpen","InstancePropertyStoreOpen","InstancePropertyStoreOpen method","InstancePropertyStoreOpen method","IFunctionDiscoveryProvider interface","STGM_READ","STGM_READWRITE","STGM_WRITE","functiondiscoveryprovider/IFunctionDiscoveryProvider::InstancePropertyStoreOpen","ncd.ifunctiondiscoveryprovider_instancepropertystoreopen"]
old-location: ncd\ifunctiondiscoveryprovider_instancepropertystoreopen.htm
tech.root: ncd
ms.assetid: 35e98e8a-5e6c-4cbb-9a61-9720f11f90d6
ms.date: 12/05/2018
ms.keywords: IFunctionDiscoveryProvider interface,InstancePropertyStoreOpen method, IFunctionDiscoveryProvider.InstancePropertyStoreOpen, IFunctionDiscoveryProvider::InstancePropertyStoreOpen, InstancePropertyStoreOpen, InstancePropertyStoreOpen method, InstancePropertyStoreOpen method,IFunctionDiscoveryProvider interface, STGM_READ, STGM_READWRITE, STGM_WRITE, functiondiscoveryprovider/IFunctionDiscoveryProvider::InstancePropertyStoreOpen, ncd.ifunctiondiscoveryprovider_instancepropertystoreopen
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFunctionDiscoveryProvider::InstancePropertyStoreOpen
 - functiondiscoveryprovider/IFunctionDiscoveryProvider::InstancePropertyStoreOpen
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FunctionDiscoveryProvider.h
api_name:
 - IFunctionDiscoveryProvider.InstancePropertyStoreOpen
---

# IFunctionDiscoveryProvider::InstancePropertyStoreOpen


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Opens the property store of the provider. This method is called whenever <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctioninstance-openpropertystore">IFunctionInstance::OpenPropertyStore</a> is called if the provider did not provide a property store at creation time.  The provider can provide the property store at this time, or handle the <a href="/windows/desktop/api/functiondiscoveryprovider/nn-functiondiscoveryprovider-iproviderproperties">IProviderProperties</a> methods as they are called.

## -parameters

### -param pIFunctionInstance [in]

A pointer to the <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctioninstance">IFunctionInstance</a> interface for the store that is to be opened. Each property store is associated with a function instance.

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
The method could not open a writable property store because the caller has insufficient access, the discovery provider does not allow write access to its property store, or another property store is already open for this function instance.

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

<a href="/windows/desktop/api/functiondiscoveryprovider/nn-functiondiscoveryprovider-ifunctiondiscoveryprovider">IFunctionDiscoveryProvider</a>