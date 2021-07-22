---
UID: NF:functiondiscoveryprovider.IFunctionDiscoveryProviderFactory.CreateInstance
title: IFunctionDiscoveryProviderFactory::CreateInstance (functiondiscoveryprovider.h)
description: Creates a function instance.
helpviewer_keywords: ["CreateInstance","CreateInstance method","CreateInstance method","IFunctionDiscoveryProviderFactory interface","IFunctionDiscoveryProviderFactory interface","CreateInstance method","IFunctionDiscoveryProviderFactory.CreateInstance","IFunctionDiscoveryProviderFactory::CreateInstance","functiondiscoveryprovider/IFunctionDiscoveryProviderFactory::CreateInstance","ncd.ifunctiondiscoveryproviderfactory_createinstance"]
old-location: ncd\ifunctiondiscoveryproviderfactory_createinstance.htm
tech.root: ncd
ms.assetid: 143a4f62-7093-4127-b89e-e7d0985a92bb
ms.date: 12/05/2018
ms.keywords: CreateInstance, CreateInstance method, CreateInstance method,IFunctionDiscoveryProviderFactory interface, IFunctionDiscoveryProviderFactory interface,CreateInstance method, IFunctionDiscoveryProviderFactory.CreateInstance, IFunctionDiscoveryProviderFactory::CreateInstance, functiondiscoveryprovider/IFunctionDiscoveryProviderFactory::CreateInstance, ncd.ifunctiondiscoveryproviderfactory_createinstance
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
 - IFunctionDiscoveryProviderFactory::CreateInstance
 - functiondiscoveryprovider/IFunctionDiscoveryProviderFactory::CreateInstance
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
 - IFunctionDiscoveryProviderFactory.CreateInstance
---

# IFunctionDiscoveryProviderFactory::CreateInstance


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Creates a function instance. All function instances should be created using this method.  Other implementations that support <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctioninstance">IFunctionInstance</a> should not be used.

## -parameters

### -param pszSubCategory [in]

The subcategory string for the function instance. See <a href="/previous-versions/windows/desktop/fundisc/subcategory-definitions">Subcategory Definitions</a>.

### -param pszProviderInstanceIdentity [in]

The provider instance identifier.  

Function Discovery uses this identifier to ensure that function instance identifiers returned by <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctioninstance-getid">IFunctionInstance::GetID</a> are unique.  To that end, Function Discovery attaches a prefix to the identifier passed to <i>pszProviderInstanceIdentity</i> to ensure that a given function instance identifier is unique across all providers. Implementers only need to ensure that <i>pszProviderInstanceIdentity</i> uniquely identifies the device, resource, or instance within the scope of the provider.

This string  is returned to client applications that call  <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctioninstance-getproviderinstanceid">IFunctionInstance::GetProviderInstanceID</a>.

There is no upper limit on the size of this string.

### -param iProviderInstanceContext [in]

The context associated with the specific function instance.

### -param pIPropertyStore [in]

A pointer to an <b>IPropertyStore</b> interface.

### -param pIFunctionDiscoveryProvider [in]

A pointer to the <a href="/windows/desktop/api/functiondiscoveryprovider/nn-functiondiscoveryprovider-ifunctiondiscoveryprovider">IFunctionDiscoveryProvider</a> provider instance creating this function instance.

### -param ppIFunctionInstance [out]

A pointer to an <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctioninstance">IFunctionInstance</a> interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The provider should specify the subcategory (may be <b>NULL</b>), the instance identifier, a provider-allocated context (if required), and an optional property store.  

<b>CreateInstance</b> returns an appropriately initialized function instance to the provider.

The context specified by the provider will be passed back to the provider for all subsequent function instance related methods, such as <a href="/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-ifunctiondiscoveryprovider-instancereleased">InstanceReleased</a>, <a href="/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-ifunctiondiscoveryprovider-instancepropertystoreopen">InstancePropertyStoreOpen</a>, <a href="/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-ifunctiondiscoveryprovider-instancepropertystoreflush">InstancePropertyStoreFlush</a>, and <a href="/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-ifunctiondiscoveryprovider-instancequeryservice">InstanceQueryService</a>.

The provider must guarantee that the provider reference count does not go to zero, possibly on another thread, while <b>CreateInstance</b>  is being called.

## -see-also

<a href="/windows/desktop/api/functiondiscoveryprovider/nn-functiondiscoveryprovider-ifunctiondiscoveryproviderfactory">IFunctionDiscoveryProviderFactory</a>