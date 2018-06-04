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

# IAzAuthorizationStore::UpdateCache


## -description


The <b>UpdateCache</b> method updates the cache of objects and object attributes to match the underlying policy store.


## -parameters




### -param varReserved [in, optional]

Reserved for future use.


## -remarks



When the <b>UpdateCache</b> method is called, all changes to the persistent store after the last call to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a> method or to the <b>UpdateCache</b> method are incorporated into the cache. Any changes to the cache that have not been submitted using the <a href="https://msdn.microsoft.com/bf2962af-0e8f-4c4c-a63a-dfd623308e4d">Submit</a> method override the changes to the  store.

Most stores  should be  stable and have  few changes.  Providers are expected to implement this method to efficiently  determine whether   changes have been written  to the physical store since the last update.



