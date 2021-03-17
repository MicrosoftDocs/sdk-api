---
UID: NS:http._HTTP_BINDING_INFO
title: HTTP_BINDING_INFO (http.h)
description: Used to associate a URL Group with a request queue.
helpviewer_keywords: ["*PHTTP_BINDING_INFO","*PHTTP_BINDING_INFO structure [HTTP]","HTTP_BINDING_INFO","HTTP_BINDING_INFO structure [HTTP]","http.http_binding_info","http/*PHTTP_BINDING_INFO","http/HTTP_BINDING_INFO"]
old-location: http\http_binding_info.htm
tech.root: http
ms.assetid: 551a928a-84c6-479b-a500-de69dc8857cd
ms.date: 12/05/2018
ms.keywords: '*PHTTP_BINDING_INFO, *PHTTP_BINDING_INFO structure [HTTP], HTTP_BINDING_INFO, HTTP_BINDING_INFO structure [HTTP], http.http_binding_info, http/*PHTTP_BINDING_INFO, http/HTTP_BINDING_INFO'
req.header: http.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: HTTP_BINDING_INFO, *PHTTP_BINDING_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_BINDING_INFO
 - http/_HTTP_BINDING_INFO
 - PHTTP_BINDING_INFO
 - http/PHTTP_BINDING_INFO
 - HTTP_BINDING_INFO
 - http/HTTP_BINDING_INFO
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
 - HTTP_BINDING_INFO
---

# HTTP_BINDING_INFO structure


## -description

The <b>HTTP_BINDING_INFO</b> structure is used to associate a URL Group with a request queue.

This structure must be used when setting or querying the <a href="/windows/desktop/api/http/ne-http-http_server_property">HttpServerBindingProperty</a> on a URL Group.

## -struct-fields

### -field Flags

The <a href="/windows/desktop/api/http/ns-http-http_property_flags">HTTP_PROPERTY_FLAGS</a> structure specifying whether the property is present.

### -field RequestQueueHandle

The request queue that is associated with the URL group. The structure can be used to remove an existing binding by setting this parameter to <b>NULL</b>.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-2-0-structures">HTTP Server API Version 2.0 Structures</a>



<a href="/windows/desktop/api/http/ne-http-http_server_property">HTTP_SERVER_PROPERTY</a>



<a href="/windows/desktop/api/http/nf-http-httpqueryurlgroupproperty">HttpQueryUrlGroupProperty</a>



<a href="/windows/desktop/api/http/nf-http-httpseturlgroupproperty">HttpSetUrlGroupProperty</a>