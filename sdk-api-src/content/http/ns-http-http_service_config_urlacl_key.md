---
UID: NS:http._HTTP_SERVICE_CONFIG_URLACL_KEY
title: HTTP_SERVICE_CONFIG_URLACL_KEY (http.h)
description: Used to specify a particular reservation record in the URL namespace reservation store.
helpviewer_keywords: ["*PHTTP_SERVICE_CONFIG_URLACL_KEY","HTTP_SERVICE_CONFIG_URLACL_KEY","HTTP_SERVICE_CONFIG_URLACL_KEY structure [HTTP]","PHTTP_SERVICE_CONFIG_URLACL_KEY","PHTTP_SERVICE_CONFIG_URLACL_KEY structure pointer [HTTP]","_http_http_service_config_urlacl_key","http.http_service_config_urlacl_key","http/HTTP_SERVICE_CONFIG_URLACL_KEY","http/PHTTP_SERVICE_CONFIG_URLACL_KEY"]
old-location: http\http_service_config_urlacl_key.htm
tech.root: http
ms.assetid: ab739046-c25c-43bd-8c1f-da3aab374a05
ms.date: 12/05/2018
ms.keywords: '*PHTTP_SERVICE_CONFIG_URLACL_KEY, HTTP_SERVICE_CONFIG_URLACL_KEY, HTTP_SERVICE_CONFIG_URLACL_KEY structure [HTTP], PHTTP_SERVICE_CONFIG_URLACL_KEY, PHTTP_SERVICE_CONFIG_URLACL_KEY structure pointer [HTTP], _http_http_service_config_urlacl_key, http.http_service_config_urlacl_key, http/HTTP_SERVICE_CONFIG_URLACL_KEY, http/PHTTP_SERVICE_CONFIG_URLACL_KEY'
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
req.typenames: HTTP_SERVICE_CONFIG_URLACL_KEY, *PHTTP_SERVICE_CONFIG_URLACL_KEY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_SERVICE_CONFIG_URLACL_KEY
 - http/_HTTP_SERVICE_CONFIG_URLACL_KEY
 - PHTTP_SERVICE_CONFIG_URLACL_KEY
 - http/PHTTP_SERVICE_CONFIG_URLACL_KEY
 - HTTP_SERVICE_CONFIG_URLACL_KEY
 - http/HTTP_SERVICE_CONFIG_URLACL_KEY
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
 - HTTP_SERVICE_CONFIG_URLACL_KEY
---

# HTTP_SERVICE_CONFIG_URLACL_KEY structure


## -description

The 
<b>HTTP_SERVICE_CONFIG_URLACL_KEY</b> structure is used to specify a particular reservation record in the URL namespace reservation store. It is a member of the 
<a href="/windows/desktop/api/http/ns-http-http_service_config_urlacl_set">HTTP_SERVICE_CONFIG_URLACL_SET</a> and 
<a href="/windows/desktop/api/http/ns-http-http_service_config_urlacl_query">HTTP_SERVICE_CONFIG_URLACL_QUERY</a> structures.

## -struct-fields

### -field pUrlPrefix

A pointer to the 
<a href="/windows/desktop/Http/urlprefix-strings">UrlPrefix string</a> that defines the portion of the URL namespace to which this reservation pertains.

## -see-also

<a href="/windows/desktop/api/http/ns-http-http_service_config_urlacl_query">HTTP_SERVICE_CONFIG_URLACL_QUERY</a>



<a href="/windows/desktop/api/http/ns-http-http_service_config_urlacl_set">HTTP_SERVICE_CONFIG_URLACL_SET</a>



<a href="/windows/desktop/Http/urlprefix-strings">UrlPrefix Strings</a>