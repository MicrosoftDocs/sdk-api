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

# _HTTP_CACHE_POLICY structure


## -description


The 
<b>HTTP_CACHE_POLICY</b> structure is used to define a cache policy associated with a cached response fragment.


## -struct-fields




### -field Policy

This parameter is one of the following values from the <a href="https://msdn.microsoft.com/07d9853f-d38c-4e5b-815a-3dc0157b4d8d">HTTP_CACHE_POLICY_TYPE</a> to control how an associated response or response fragment is cached.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HttpCachePolicyNocache"></a><a id="httpcachepolicynocache"></a><a id="HTTPCACHEPOLICYNOCACHE"></a><dl>
<dt><b>HttpCachePolicyNocache</b></dt>
</dl>
</td>
<td width="60%">
Do not cache the data at all.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpCachePolicyUserInvalidates"></a><a id="httpcachepolicyuserinvalidates"></a><a id="HTTPCACHEPOLICYUSERINVALIDATES"></a><dl>
<dt><b>HttpCachePolicyUserInvalidates</b></dt>
</dl>
</td>
<td width="60%">
Cache the data until the application explicitly releases it.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpCachePolicyTimeToLive"></a><a id="httpcachepolicytimetolive"></a><a id="HTTPCACHEPOLICYTIMETOLIVE"></a><dl>
<dt><b>HttpCachePolicyTimeToLive</b></dt>
</dl>
</td>
<td width="60%">
Cache the data for a number of seconds specified by the <b>SecondsToLive</b> member.

</td>
</tr>
</table>
 


### -field SecondsToLive

When the <b>Policy</b> member is equal to HttpCachePolicyTimeToLive, data is cached for <b>SecondsToLive</b> seconds before it is released. For other values of <b>Policy</b>, <b>SecondsToLive</b> is ignored.


## -see-also




<a href="https://msdn.microsoft.com/caef2e93-39cd-4282-97d9-870f8236d8c4">HttpAddFragmentToCache</a>
 

 

