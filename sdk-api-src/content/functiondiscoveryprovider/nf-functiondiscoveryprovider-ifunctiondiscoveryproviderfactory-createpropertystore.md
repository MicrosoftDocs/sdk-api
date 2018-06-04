---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

