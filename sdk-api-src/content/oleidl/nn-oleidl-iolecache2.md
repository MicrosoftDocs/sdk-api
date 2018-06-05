---
UID: NN:oleidl.IOleCache2
title: IOleCache2
author: windows-sdk-content
description: Enables object clients to selectively update each cache that was created with IOleCache::Cache.
old-location: com\iolecache2.htm
old-project: com
ms.assetid: 8bbeca2d-c805-4116-b918-e2ddded8b160
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IOleCache2, IOleCache2 interface [COM], IOleCache2 interface [COM],described, _ole_iolecache2, com.iolecache2, oleidl/IOleCache2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: USERCLASSTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	OleIdl.h
api_name:
-	IOleCache2
product: Windows
targetos: Windows
req.lib: 
req.dll: Adhocreportingexcelclient.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOleCache2 interface


## -description


Enables object clients to selectively update each cache that was created with <a href="https://msdn.microsoft.com/2a86063a-3ee6-4fc2-a6e0-6e9ffa658348">IOleCache::Cache</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOleCache2</b> interface inherits from <b>IOleCache</b>. <b>IOleCache2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOleCache2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/03fb4bdb-1655-4923-b124-8854419766ec">DiscardCache</a>
</td>
<td align="left" width="63%">
Discards the caches found in memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/67bb0bcf-981a-4b2f-8ab9-2afc0659b2db">UpdateCache</a>
</td>
<td align="left" width="63%">
Updates the specified caches.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/8a64675b-1337-4555-b9a6-e19f9b987ba2">CreateDataCache</a>



<a href="https://msdn.microsoft.com/b5ef85d0-b54e-4831-87f1-ac6763179181">IOleCache</a>



<a href="https://msdn.microsoft.com/64cc7a29-0bbb-4535-a7b5-9b1d82ad7e8a">IOleCacheControl</a>
 

 

