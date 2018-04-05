---
UID: NF:oleidl.IOleCache.EnumCache
title: IOleCache::EnumCache method
author: windows-driver-content
description: Creates an enumerator that can be used to enumerate the current cache connections.
old-location: com\iolecache_enumcache.htm
old-project: com
ms.assetid: a8d99926-8fb9-4624-8025-483101cb9311
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: EnumCache method [COM], EnumCache method [COM], IOleCache interface, EnumCache,IOleCache.EnumCache, IOleCache, IOleCache interface [COM], EnumCache method, IOleCache::EnumCache, _ole_iolecache_enumcache, com.iolecache_enumcache, oleidl/IOleCache::EnumCache
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: USERCLASSTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	OleIdl.h
api_name:
-	IOleCache.EnumCache
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IOleCache::EnumCache method


## -description


Creates an enumerator that can be used to enumerate the current cache connections.


## -parameters




### -param ppenumSTATDATA [out]

A pointer to an <a href="https://msdn.microsoft.com/8e2f6655-4a09-4868-a909-18999104b3ff">IEnumSTATDATA</a> pointer variable that receives the interface pointer to the new enumerator object. If this parameter is <b>NULL</b>, there are no cache connections at this time.


## -returns



This method returns S_OK if enumerator object is successfully instantiated or there are no cache connections.

<div class="alert"><b>Note</b>  Check the <i>ppenumSTATDATA</i> parameter to determine which result occurred. If the <i>ppenumSTATDATA</i> parameter is <b>NULL</b>, then there are no cache connections at this time.</div>
<div> </div>



## -remarks



The enumerator object returned by this method implements the <a href="https://msdn.microsoft.com/8e2f6655-4a09-4868-a909-18999104b3ff">IEnumSTATDATA</a> interface. <b>IEnumSTATDATA</b> enumerates the data stored in an array of <a href="https://msdn.microsoft.com/f31469b2-4a4a-4da5-9229-38ddd0bcc88e">STATDATA</a> structures containing information about current cache connections.




## -see-also




<a href="https://msdn.microsoft.com/8e2f6655-4a09-4868-a909-18999104b3ff">IEnumSTATDATA</a>



<a href="https://msdn.microsoft.com/b5ef85d0-b54e-4831-87f1-ac6763179181">IOleCache</a>



<a href="https://msdn.microsoft.com/2a86063a-3ee6-4fc2-a6e0-6e9ffa658348">IOleCache::Cache</a>
 

 

