---
UID: NN:functiondiscoveryprovider.IProviderProperties
title: IProviderProperties (functiondiscoveryprovider.h)
description: Is optionally implemented by discovery providers to directly create and manage their own property store.
helpviewer_keywords: ["IProviderProperties","IProviderProperties interface","IProviderProperties interface","described","functiondiscoveryprovider/IProviderProperties","ncd.iproviderproperties"]
old-location: ncd\iproviderproperties.htm
tech.root: ncd
ms.assetid: d6d3d1d1-d2fb-409c-be37-3cd286e325a3
ms.date: 12/05/2018
ms.keywords: IProviderProperties, IProviderProperties interface, IProviderProperties interface,described, functiondiscoveryprovider/IProviderProperties, ncd.iproviderproperties
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
 - IProviderProperties
 - functiondiscoveryprovider/IProviderProperties
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
 - IProviderProperties
---

# IProviderProperties interface


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

This interface is optionally implemented by discovery providers to directly create and manage their own property store. If this interface is implemented, the provider can use its property store for its own internal use, but all queries from the property store implemented by this interface will go directly to the provider, and the internal property store will never be exposed to a client calling <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctioninstance-openpropertystore">IFunctionInstance::OpenPropertyStore</a>.

## -inheritance

The <b>IProviderProperties</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IProviderProperties</b> also has these types of members:

## -remarks

Implementing this interface enables a provider to provide access to the most current property values. Otherwise, the client uses the values in the cache created by Function Discovery when the function instance is created or the property store is opened.

If a provider does not implement this interface, then the provider must provide a property store
at the time the instance is created or when the client calls <a href="/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-ifunctiondiscoveryprovider-instancepropertystoreopen">InstancePropertyStoreOpen</a>.

## -see-also

<a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a>
