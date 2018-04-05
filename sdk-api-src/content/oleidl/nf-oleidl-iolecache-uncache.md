---
UID: NF:oleidl.IOleCache.Uncache
title: IOleCache::Uncache method
author: windows-driver-content
description: Removes a cache connection created previously using IOleCache::Cache.
old-location: com\iolecache_uncache.htm
old-project: com
ms.assetid: a6a57bdd-190f-485b-9b46-cbfc1a1d29a6
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IOleCache, IOleCache interface [COM], Uncache method, IOleCache::Uncache, Uncache method [COM], Uncache method [COM], IOleCache interface, Uncache,IOleCache.Uncache, _ole_iolecache_uncache, com.iolecache_uncache, oleidl/IOleCache::Uncache
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
-	IOleCache.Uncache
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IOleCache::Uncache method


## -description


Removes a cache connection created previously using <a href="https://msdn.microsoft.com/2a86063a-3ee6-4fc2-a6e0-6e9ffa658348">IOleCache::Cache</a>.


## -parameters




### -param dwConnection [in]

The cache connection to be removed. This nonzero value was returned by <a href="https://msdn.microsoft.com/2a86063a-3ee6-4fc2-a6e0-6e9ffa658348">IOleCache::Cache</a> when the cache was originally established.


## -returns



This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_NOCONNECTION</b></dt>
</dl>
</td>
<td width="60%">
No cache connection exists for <i>dwConnection</i>.

</td>
</tr>
</table>
 




## -remarks



The <b>IOleCache::Uncache</b> method removes a cache connection that was created in a prior call to <a href="https://msdn.microsoft.com/2a86063a-3ee6-4fc2-a6e0-6e9ffa658348">IOleCache::Cache</a>. It uses the <i>dwConnection</i> parameter that was returned by the prior call to <b>IOleCache::Cache</b>.




## -see-also




<a href="https://msdn.microsoft.com/b5ef85d0-b54e-4831-87f1-ac6763179181">IOleCache</a>



<a href="https://msdn.microsoft.com/2a86063a-3ee6-4fc2-a6e0-6e9ffa658348">IOleCache::Cache</a>
 

 

