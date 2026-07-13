---
UID: NF:functiondiscoveryprovider.IFunctionDiscoveryProviderFactory.CreatePropertyStore
title: IFunctionDiscoveryProviderFactory::CreatePropertyStore (functiondiscoveryprovider.h)
description: Enables providers to reuse the in-memory property store implementation.
helpviewer_keywords: ["CreatePropertyStore","CreatePropertyStore method","CreatePropertyStore method","IFunctionDiscoveryProviderFactory interface","IFunctionDiscoveryProviderFactory interface","CreatePropertyStore method","IFunctionDiscoveryProviderFactory.CreatePropertyStore","IFunctionDiscoveryProviderFactory::CreatePropertyStore","functiondiscoveryprovider/IFunctionDiscoveryProviderFactory::CreatePropertyStore","ncd.ifunctiondiscoveryproviderfactory_createpropertystore"]
old-location: ncd\ifunctiondiscoveryproviderfactory_createpropertystore.htm
tech.root: ncd
ms.assetid: 668d0a70-a0c1-4e43-a258-5221e3fe28a1
ms.date: 12/05/2018
ms.keywords: CreatePropertyStore, CreatePropertyStore method, CreatePropertyStore method,IFunctionDiscoveryProviderFactory interface, IFunctionDiscoveryProviderFactory interface,CreatePropertyStore method, IFunctionDiscoveryProviderFactory.CreatePropertyStore, IFunctionDiscoveryProviderFactory::CreatePropertyStore, functiondiscoveryprovider/IFunctionDiscoveryProviderFactory::CreatePropertyStore, ncd.ifunctiondiscoveryproviderfactory_createpropertystore
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
 - IFunctionDiscoveryProviderFactory::CreatePropertyStore
 - functiondiscoveryprovider/IFunctionDiscoveryProviderFactory::CreatePropertyStore
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
 - IFunctionDiscoveryProviderFactory.CreatePropertyStore
---

# IFunctionDiscoveryProviderFactory::CreatePropertyStore


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Enables providers to reuse the in-memory property store implementation.

## -parameters

### -param ppIPropertyStore [out]

A pointer to an <b>IPropertyStore</b> interface pointer.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

 If providers wish to cache properties, either when the function instance is created or when the property store is first opened, the provider can use this method to create an in memory property store, set properties as necessary, and then either assign it to the function instance at creation time using <a href="/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-ifunctiondiscoveryproviderfactory-createinstance">CreateInstance</a> or when the property store is first opened using <a href="/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-ifunctiondiscoveryprovider-instancepropertystoreopen">InstancePropertyStoreOpen</a>.

## -see-also

<a href="/windows/desktop/api/functiondiscoveryprovider/nn-functiondiscoveryprovider-ifunctiondiscoveryproviderfactory">IFunctionDiscoveryProviderFactory</a>