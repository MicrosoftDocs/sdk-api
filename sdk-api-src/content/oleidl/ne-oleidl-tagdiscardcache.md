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

# tagDISCARDCACHE enumeration


## -description


Specifies what to do with caches that are to be discarded from memory if their dirty bit has been set.


## -enum-fields




### -field DISCARDCACHE_SAVEIFDIRTY

The cache is to be saved to disk.


### -field DISCARDCACHE_NOSAVE

The cache can be discarded without saving it.



## -see-also




<a href="https://msdn.microsoft.com/03fb4bdb-1655-4923-b124-8854419766ec">IOleCache2::DiscardCache</a>
 

 

