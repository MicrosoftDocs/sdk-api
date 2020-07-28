---
UID: NF:azroles.IAzAuthorizationStore.UpdateCache
title: IAzAuthorizationStore::UpdateCache (azroles.h)
description: Updates the cache of objects and object attributes to match the underlying policy store.
helpviewer_keywords: ["AzAuthorizationStore object [Security]","UpdateCache method","IAzAuthorizationStore interface [Security]","UpdateCache method","IAzAuthorizationStore.UpdateCache","IAzAuthorizationStore::UpdateCache","UpdateCache","UpdateCache method [Security]","UpdateCache method [Security]","AzAuthorizationStore object","UpdateCache method [Security]","IAzAuthorizationStore interface","azroles/IAzAuthorizationStore::UpdateCache","security.azauthorizationstore_updatecache"]
old-location: security\azauthorizationstore_updatecache.htm
tech.root: security
ms.assetid: 1fd17040-f736-44a6-8a01-720f4c8fe9ac
ms.date: 12/05/2018
ms.keywords: AzAuthorizationStore object [Security],UpdateCache method, IAzAuthorizationStore interface [Security],UpdateCache method, IAzAuthorizationStore.UpdateCache, IAzAuthorizationStore::UpdateCache, UpdateCache, UpdateCache method [Security], UpdateCache method [Security],AzAuthorizationStore object, UpdateCache method [Security],IAzAuthorizationStore interface, azroles/IAzAuthorizationStore::UpdateCache, security.azauthorizationstore_updatecache
f1_keywords:
- azroles/AzAuthorizationStore.UpdateCache
dev_langs:
- c++
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Azroles.dll
api_name:
- AzAuthorizationStore.UpdateCache
- IAzAuthorizationStore.UpdateCache
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
---

# IAzAuthorizationStore::UpdateCache


## -description


The <b>UpdateCache</b> method updates the cache of objects and object attributes to match the underlying policy store.


## -parameters




### -param varReserved [in, optional]

Reserved for future use.


## -remarks



When the <b>UpdateCache</b> method is called, all changes to the persistent store after the last call to the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-initialize">Initialize</a> method or to the <b>UpdateCache</b> method are incorporated into the cache. Any changes to the cache that have not been submitted using the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-submit">Submit</a> method override the changes to the  store.

Most stores  should be  stable and have  few changes.  Providers are expected to implement this method to efficiently  determine whether   changes have been written  to the physical store since the last update.



