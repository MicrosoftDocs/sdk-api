---
UID: NF:identitystore.IIdentityStore.AddToCache
title: IIdentityStore::AddToCache
author: windows-sdk-content
description: Caches the specified identity in the registry.
old-location: security\iidentitystore_addtocache.htm
tech.root: secauthn
ms.assetid: 5ce977bc-41fa-4f80-bb82-76a8bdc40e7e
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: AddToCache, AddToCache method [Security], AddToCache method [Security],IIdentityStore interface, IIdentityStore interface [Security],AddToCache method, IIdentityStore.AddToCache, IIdentityStore::AddToCache, identitystore/IIdentityStore::AddToCache, security.iidentitystore_addtocache
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: identitystore.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Identitystore.idl
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
 - Identitystore.h
api_name:
 - IIdentityStore.AddToCache
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IIdentityStore::AddToCache


## -description


The <b>AddtoCache</b> method caches the specified identity in the registry.


## -parameters




### -param lpszUniqueID [in]

The identity to cache.


### -param ProviderGUID [in]

The identity provider associated with the identity.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/f7f0f103-411b-4fbd-9ed5-30c6ab2f0ab6">IIdentityStore</a>
 

 

