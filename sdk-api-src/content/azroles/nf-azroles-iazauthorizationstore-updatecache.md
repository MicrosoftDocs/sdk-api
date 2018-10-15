---
UID: NF:azroles.IAzAuthorizationStore.UpdateCache
title: IAzAuthorizationStore::UpdateCache
author: windows-sdk-content
description: Updates the cache of objects and object attributes to match the underlying policy store.
old-location: security\azauthorizationstore_updatecache.htm
tech.root: SecAuthZ
ms.assetid: 1fd17040-f736-44a6-8a01-720f4c8fe9ac
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: AzAuthorizationStore object [Security],UpdateCache method, IAzAuthorizationStore interface [Security],UpdateCache method, IAzAuthorizationStore.UpdateCache, IAzAuthorizationStore::UpdateCache, UpdateCache, UpdateCache method [Security], UpdateCache method [Security],AzAuthorizationStore object, UpdateCache method [Security],IAzAuthorizationStore interface, azroles/IAzAuthorizationStore::UpdateCache, security.azauthorizationstore_updatecache
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzAuthorizationStore::UpdateCache


## -description


The <b>UpdateCache</b> method updates the cache of objects and object attributes to match the underlying policy store.


## -parameters




### -param varReserved [in, optional]

Reserved for future use.


## -remarks



When the <b>UpdateCache</b> method is called, all changes to the persistent store after the last call to the <a href="https://msdn.microsoft.com/c461d50a-c785-4b32-b331-fe3a1693f4de">Initialize</a> method or to the <b>UpdateCache</b> method are incorporated into the cache. Any changes to the cache that have not been submitted using the <a href="https://msdn.microsoft.com/bf2962af-0e8f-4c4c-a63a-dfd623308e4d">Submit</a> method override the changes to the  store.

Most stores  should be  stable and have  few changes.  Providers are expected to implement this method to efficiently  determine whether   changes have been written  to the physical store since the last update.



