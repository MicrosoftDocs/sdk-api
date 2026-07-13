---
UID: NF:functiondiscoveryprovider.IFunctionDiscoveryProvider.InstancePropertyStoreValidateAccess
title: IFunctionDiscoveryProvider::InstancePropertyStoreValidateAccess (functiondiscoveryprovider.h)
description: Verifies that the provider supports the requested access.
helpviewer_keywords: ["IFunctionDiscoveryProvider interface","InstancePropertyStoreValidateAccess method","IFunctionDiscoveryProvider.InstancePropertyStoreValidateAccess","IFunctionDiscoveryProvider::InstancePropertyStoreValidateAccess","InstancePropertyStoreValidateAccess","InstancePropertyStoreValidateAccess method","InstancePropertyStoreValidateAccess method","IFunctionDiscoveryProvider interface","STGM_READ","STGM_READWRITE","STGM_WRITE","functiondiscoveryprovider/IFunctionDiscoveryProvider::InstancePropertyStoreValidateAccess","ncd.ifunctiondiscoveryprovider_instancepropertystorevalidateaccess"]
old-location: ncd\ifunctiondiscoveryprovider_instancepropertystorevalidateaccess.htm
tech.root: ncd
ms.assetid: 0ee8d65d-0be3-4171-946a-10a15b8f8eb7
ms.date: 12/05/2018
ms.keywords: IFunctionDiscoveryProvider interface,InstancePropertyStoreValidateAccess method, IFunctionDiscoveryProvider.InstancePropertyStoreValidateAccess, IFunctionDiscoveryProvider::InstancePropertyStoreValidateAccess, InstancePropertyStoreValidateAccess, InstancePropertyStoreValidateAccess method, InstancePropertyStoreValidateAccess method,IFunctionDiscoveryProvider interface, STGM_READ, STGM_READWRITE, STGM_WRITE, functiondiscoveryprovider/IFunctionDiscoveryProvider::InstancePropertyStoreValidateAccess, ncd.ifunctiondiscoveryprovider_instancepropertystorevalidateaccess
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
 - IFunctionDiscoveryProvider::InstancePropertyStoreValidateAccess
 - functiondiscoveryprovider/IFunctionDiscoveryProvider::InstancePropertyStoreValidateAccess
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
 - IFunctionDiscoveryProvider.InstancePropertyStoreValidateAccess
---

# IFunctionDiscoveryProvider::InstancePropertyStoreValidateAccess


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Verifies that the provider supports the  requested access. It is called when <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctioninstance-openpropertystore">OpenPropertyStore</a> is called on a function instance to verify that the provider supports the access mode passed by the <i>dwStgAccess</i> parameter.   

This method is only called when a provider's <a href="/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-ifunctiondiscoveryprovider-initialize">Initialize</a> method returns  a <i>pdwStgAccessCapabilities</i> parameter value of -1.

## -parameters

### -param pIFunctionInstance [in]

A pointer to the <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctioninstance">IFunctionInstance</a> interface.

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

<a href="/windows/desktop/api/functiondiscoveryprovider/nn-functiondiscoveryprovider-ifunctiondiscoveryprovider">IFunctionDiscoveryProvider</a>