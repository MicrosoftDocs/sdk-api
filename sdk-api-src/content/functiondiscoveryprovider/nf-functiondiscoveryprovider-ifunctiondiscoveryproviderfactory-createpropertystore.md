---
UID: NF:functiondiscoveryprovider.IFunctionDiscoveryProviderFactory.CreatePropertyStore
title: IFunctionDiscoveryProviderFactory::CreatePropertyStore
author: windows-sdk-content
description: Enables providers to reuse the in-memory property store implementation.
old-location: ncd\ifunctiondiscoveryproviderfactory_createpropertystore.htm
tech.root: fundisc
ms.assetid: 668d0a70-a0c1-4e43-a258-5221e3fe28a1
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: CreatePropertyStore, CreatePropertyStore method, CreatePropertyStore method,IFunctionDiscoveryProviderFactory interface, IFunctionDiscoveryProviderFactory interface,CreatePropertyStore method, IFunctionDiscoveryProviderFactory.CreatePropertyStore, IFunctionDiscoveryProviderFactory::CreatePropertyStore, functiondiscoveryprovider/IFunctionDiscoveryProviderFactory::CreatePropertyStore, ncd.ifunctiondiscoveryproviderfactory_createpropertystore
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
 - IFunctionDiscoveryProviderFactory.CreatePropertyStore
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFunctionDiscoveryProviderFactory::CreatePropertyStore


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Enables providers to reuse the in-memory property store implementation.


## -parameters




### -param ppIPropertyStore [out]

A pointer to an <b>IPropertyStore</b> interface pointer.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



 If providers wish to cache properties, either when the function instance is created or when the property store is first opened, the provider can use this method to create an in memory property store, set properties as necessary, and then either assign it to the function instance at creation time using <a href="https://msdn.microsoft.com/143a4f62-7093-4127-b89e-e7d0985a92bb">CreateInstance</a> or when the property store is first opened using <a href="https://msdn.microsoft.com/35e98e8a-5e6c-4cbb-9a61-9720f11f90d6">InstancePropertyStoreOpen</a>.




## -see-also




<a href="https://msdn.microsoft.com/576db617-0bca-4b46-839b-0f133f28cacb">IFunctionDiscoveryProviderFactory</a>
 

 

