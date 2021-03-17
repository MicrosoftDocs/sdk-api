---
UID: NE:http._HTTP_CACHE_POLICY_TYPE
title: HTTP_CACHE_POLICY_TYPE (http.h)
description: The HTTP_CACHE_POLICY_TYPE enumeration type defines available cache policies.
helpviewer_keywords: ["*PHTTP_CACHE_POLICY_TYPE","HTTP_CACHE_POLICY_TYPE","HTTP_CACHE_POLICY_TYPE enumeration [HTTP]","HttpCachePolicyMaximum","HttpCachePolicyNocache","HttpCachePolicyTimeToLive","HttpCachePolicyUserInvalidates","PHTTP_CACHE_POLICY_TYPE","PHTTP_CACHE_POLICY_TYPE enumeration pointer [HTTP]","_http_http_cache_policy_type","http.http_cache_policy_type","http/HTTP_CACHE_POLICY_TYPE","http/HttpCachePolicyMaximum","http/HttpCachePolicyNocache","http/HttpCachePolicyTimeToLive","http/HttpCachePolicyUserInvalidates","http/PHTTP_CACHE_POLICY_TYPE"]
old-location: http\http_cache_policy_type.htm
tech.root: http
ms.assetid: 07d9853f-d38c-4e5b-815a-3dc0157b4d8d
ms.date: 12/05/2018
ms.keywords: '*PHTTP_CACHE_POLICY_TYPE, HTTP_CACHE_POLICY_TYPE, HTTP_CACHE_POLICY_TYPE enumeration [HTTP], HttpCachePolicyMaximum, HttpCachePolicyNocache, HttpCachePolicyTimeToLive, HttpCachePolicyUserInvalidates, PHTTP_CACHE_POLICY_TYPE, PHTTP_CACHE_POLICY_TYPE enumeration pointer [HTTP], _http_http_cache_policy_type, http.http_cache_policy_type, http/HTTP_CACHE_POLICY_TYPE, http/HttpCachePolicyMaximum, http/HttpCachePolicyNocache, http/HttpCachePolicyTimeToLive, http/HttpCachePolicyUserInvalidates, http/PHTTP_CACHE_POLICY_TYPE'
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
req.typenames: HTTP_CACHE_POLICY_TYPE, *PHTTP_CACHE_POLICY_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_CACHE_POLICY_TYPE
 - http/_HTTP_CACHE_POLICY_TYPE
 - PHTTP_CACHE_POLICY_TYPE
 - http/PHTTP_CACHE_POLICY_TYPE
 - HTTP_CACHE_POLICY_TYPE
 - http/HTTP_CACHE_POLICY_TYPE
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
 - HTTP_CACHE_POLICY_TYPE
---

# HTTP_CACHE_POLICY_TYPE enumeration


## -description

The 
<b>HTTP_CACHE_POLICY_TYPE</b> enumeration type defines available cache policies. It is used to restrict the values of the <b>Policy</b> member of the 
<a href="/windows/desktop/api/http/ns-http-http_cache_policy">HTTP_CACHE_POLICY</a> structure, which in turn is used in the <i>pCachePolicy</i> parameter of the 
<a href="/windows/desktop/api/http/nf-http-httpaddfragmenttocache">HttpAddFragmentToCache</a> function to specify how a response fragment is cached.

## -enum-fields

### -field HttpCachePolicyNocache

Do not cache this value at all.

### -field HttpCachePolicyUserInvalidates

Cache this value until the user provides a different one.

### -field HttpCachePolicyTimeToLive

Cache this value for a specified time and then remove it from the cache.

### -field HttpCachePolicyMaximum

Terminates the enumeration; not used to determine policy.

## -see-also

<a href="/windows/desktop/api/http/ns-http-http_cache_policy">HTTP_CACHE_POLICY</a>



<a href="/windows/desktop/api/http/nf-http-httpaddfragmenttocache">HttpAddFragmentToCache</a>