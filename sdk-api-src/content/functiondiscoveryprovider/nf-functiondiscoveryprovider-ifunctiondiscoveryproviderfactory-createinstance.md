---
UID: NF:functiondiscoveryprovider.IFunctionDiscoveryProviderFactory.CreateInstance
title: IFunctionDiscoveryProviderFactory::CreateInstance
author: windows-sdk-content
description: Creates a function instance.
old-location: ncd\ifunctiondiscoveryproviderfactory_createinstance.htm
old-project: fundisc
ms.assetid: 143a4f62-7093-4127-b89e-e7d0985a92bb
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: CreateInstance, CreateInstance method, CreateInstance method,IFunctionDiscoveryProviderFactory interface, IFunctionDiscoveryProviderFactory interface,CreateInstance method, IFunctionDiscoveryProviderFactory.CreateInstance, IFunctionDiscoveryProviderFactory::CreateInstance, functiondiscoveryprovider/IFunctionDiscoveryProviderFactory::CreateInstance, ncd.ifunctiondiscoveryproviderfactory_createinstance
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: functiondiscoveryprovider.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: PropertyConstraint
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FunctionDiscoveryProvider.h
api_name:
 - IFunctionDiscoveryProviderFactory.CreateInstance
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# IFunctionDiscoveryProviderFactory::CreateInstance


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Creates a function instance. All function instances should be created using this method.  Other implementations that support <a href="https://msdn.microsoft.com/cc421719-73a6-4d4d-9bf8-171e46c4e275">IFunctionInstance</a> should not be used.


## -parameters




### -param pszSubCategory [in]

The subcategory string for the function instance. See <a href="https://msdn.microsoft.com/9793e37d-6c12-431f-95d6-fd5350f11029">Subcategory Definitions</a>.


### -param pszProviderInstanceIdentity [in]

The provider instance identifier.  

Function Discovery uses this identifier to ensure that function instance identifiers returned by <a href="https://msdn.microsoft.com/8a198bc4-cdec-4d46-a1a2-3952d4dc2a7d">IFunctionInstance::GetID</a> are unique.  To that end, Function Discovery attaches a prefix to the identifier passed to <i>pszProviderInstanceIdentity</i> to ensure that a given function instance identifier is unique across all providers. Implementers only need to ensure that <i>pszProviderInstanceIdentity</i> uniquely identifies the device, resource, or instance within the scope of the provider.

This string  is returned to client applications that call  <a href="https://msdn.microsoft.com/fad5e3f0-a440-4b09-ba8c-04bae2d14a2a">IFunctionInstance::GetProviderInstanceID</a>.

There is no upper limit on the size of this string.


### -param iProviderInstanceContext [in]

The context associated with the specific function instance.


### -param pIPropertyStore [in]

A pointer to an <b>IPropertyStore</b> interface.


### -param pIFunctionDiscoveryProvider [in]

A pointer to the <a href="https://msdn.microsoft.com/e0019d0d-1495-4a0e-a7d9-7772046a4a26">IFunctionDiscoveryProvider</a> provider instance creating this function instance. 


### -param ppIFunctionInstance [out]

A pointer to an <a href="https://msdn.microsoft.com/cc421719-73a6-4d4d-9bf8-171e46c4e275">IFunctionInstance</a> interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The provider should specify the subcategory (may be <b>NULL</b>), the instance identifier, a provider-allocated context (if required), and an optional property store.  

<b>CreateInstance</b> returns an appropriately initialized function instance to the provider.

The context specified by the provider will be passed back to the provider for all subsequent function instance related methods, such as <a href="https://msdn.microsoft.com/fa348767-8a83-4a45-9411-1e9eb545d97d">InstanceReleased</a>, <a href="https://msdn.microsoft.com/35e98e8a-5e6c-4cbb-9a61-9720f11f90d6">InstancePropertyStoreOpen</a>, <a href="https://msdn.microsoft.com/7ad29f46-fb21-4287-9fc9-9ab86d44d298">InstancePropertyStoreFlush</a>, and <a href="https://msdn.microsoft.com/8fb955dd-f396-4473-a1c1-b0d83e2b4b07">InstanceQueryService</a>.

The provider must guarantee that the provider reference count does not go to zero, possibly on another thread, while <b>CreateInstance</b>  is being called.




## -see-also




<a href="https://msdn.microsoft.com/576db617-0bca-4b46-839b-0f133f28cacb">IFunctionDiscoveryProviderFactory</a>
 

 

