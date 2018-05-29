---
UID: NN:oleidl.IOleCache
title: IOleCache
author: windows-sdk-content
description: Provides control of the presentation data that gets cached inside of an object. Cached presentation data is available to the container of the object even when the server application is not running or is unavailable.
old-location: com\iolecache.htm
old-project: com
ms.assetid: b5ef85d0-b54e-4831-87f1-ac6763179181
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IOleCache, IOleCache interface [COM], IOleCache interface [COM],described, _ole_iolecache, com.iolecache, oleidl/IOleCache
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
req.typenames: USERCLASSTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	OleIdl.h
api_name:
-	IOleCache
product: Windows
targetos: Windows
req.lib: 
req.dll: Adhocreportingexcelclient.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOleCache interface


## -description


Provides control of the presentation data that gets cached inside of an object. Cached presentation data is available to the container of the object even when the server application is not running or is unavailable.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOleCache</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IOleCache</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOleCache</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn922597">Cache</a>
</td>
<td align="left" width="63%">
Specifies the format and other data to be cached inside an embedded object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a8d99926-8fb9-4624-8025-483101cb9311">EnumCache</a>
</td>
<td align="left" width="63%">
Creates an enumerator that can be used to enumerate the current cache connections.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4b1f2fb6-636c-47dd-8f89-884f7b4f3977">InitCache</a>
</td>
<td align="left" width="63%">
Fills the cache as needed using the  data provided by the specified data object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b826411d-6e00-44ba-8603-85db40c4a55f">SetData</a>
</td>
<td align="left" width="63%">
Initializes the cache with data in a specified format and on a specified medium.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a6a57bdd-190f-485b-9b46-cbfc1a1d29a6">Uncache</a>
</td>
<td align="left" width="63%">
Removes a cache connection created previously using <a href="https://msdn.microsoft.com/2a86063a-3ee6-4fc2-a6e0-6e9ffa658348">IOleCache::Cache</a>.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/8a64675b-1337-4555-b9a6-e19f9b987ba2">CreateDataCache</a>



<a href="https://msdn.microsoft.com/8bbeca2d-c805-4116-b918-e2ddded8b160">IOleCache2</a>



<a href="https://msdn.microsoft.com/64cc7a29-0bbb-4535-a7b5-9b1d82ad7e8a">IOleCacheControl</a>
 

 

