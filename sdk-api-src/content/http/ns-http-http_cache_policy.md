---
UID: NS:http._HTTP_CACHE_POLICY
title: HTTP_CACHE_POLICY (http.h)
description: Used to define a cache policy associated with a cached response fragment.
helpviewer_keywords: ["*PHTTP_CACHE_POLICY","HTTP_CACHE_POLICY","HTTP_CACHE_POLICY structure [HTTP]","HttpCachePolicyNocache","HttpCachePolicyTimeToLive","HttpCachePolicyUserInvalidates","PHTTP_CACHE_POLICY","PHTTP_CACHE_POLICY structure pointer [HTTP]","_http_http_cache_policy","http.http_cache_policy","http/HTTP_CACHE_POLICY","http/PHTTP_CACHE_POLICY"]
old-location: http\http_cache_policy.htm
tech.root: http
ms.assetid: 91fcbf35-ef8b-4f70-9c31-3f741c0e2f6e
ms.date: 12/05/2018
ms.keywords: '*PHTTP_CACHE_POLICY, HTTP_CACHE_POLICY, HTTP_CACHE_POLICY structure [HTTP], HttpCachePolicyNocache, HttpCachePolicyTimeToLive, HttpCachePolicyUserInvalidates, PHTTP_CACHE_POLICY, PHTTP_CACHE_POLICY structure pointer [HTTP], _http_http_cache_policy, http.http_cache_policy, http/HTTP_CACHE_POLICY, http/PHTTP_CACHE_POLICY'
req.header: http.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: HTTP_CACHE_POLICY, *PHTTP_CACHE_POLICY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_CACHE_POLICY
 - http/_HTTP_CACHE_POLICY
 - PHTTP_CACHE_POLICY
 - http/PHTTP_CACHE_POLICY
 - HTTP_CACHE_POLICY
 - http/HTTP_CACHE_POLICY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Http.h
api_name:
 - HTTP_CACHE_POLICY
---

# HTTP_CACHE_POLICY structure


## -description

The 
<b>HTTP_CACHE_POLICY</b> structure is used to define a cache policy associated with a cached response fragment.

## -struct-fields

### -field Policy

This parameter is one of the following values from the <a href="/windows/desktop/api/http/ne-http-http_cache_policy_type">HTTP_CACHE_POLICY_TYPE</a> to control how an associated response or response fragment is cached.

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

<a href="/windows/desktop/api/http/nf-http-httpaddfragmenttocache">HttpAddFragmentToCache</a>