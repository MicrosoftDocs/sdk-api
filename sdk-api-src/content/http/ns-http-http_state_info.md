---
UID: NS:http._HTTP_STATE_INFO
title: HTTP_STATE_INFO (http.h)
description: Used to enable or disable a Server Session or URL Group.
helpviewer_keywords: ["*PHTTP_STATE_INFO","*PHTTP_STATE_INFO structure [HTTP]","HTTP_STATE_INFO","HTTP_STATE_INFO structure [HTTP]","http.http_state_info","http/*PHTTP_STATE_INFO","http/HTTP_STATE_INFO"]
old-location: http\http_state_info.htm
tech.root: http
ms.assetid: 736ae89b-a4fb-4962-ae68-9aaccd869c88
ms.date: 12/05/2018
ms.keywords: '*PHTTP_STATE_INFO, *PHTTP_STATE_INFO structure [HTTP], HTTP_STATE_INFO, HTTP_STATE_INFO structure [HTTP], http.http_state_info, http/*PHTTP_STATE_INFO, http/HTTP_STATE_INFO'
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
req.typenames: HTTP_STATE_INFO, *PHTTP_STATE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_STATE_INFO
 - http/_HTTP_STATE_INFO
 - PHTTP_STATE_INFO
 - http/PHTTP_STATE_INFO
 - HTTP_STATE_INFO
 - http/HTTP_STATE_INFO
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
 - HTTP_STATE_INFO
---

# HTTP_STATE_INFO structure


## -description

The <b>HTTP_STATE_INFO</b> structure is used to enable or disable a Server Session or URL Group.

This structure must be used when setting or querying the <a href="/windows/desktop/api/http/ne-http-http_server_property">HttpServerStateProperty</a> on a URL Group or Server Session.

## -struct-fields

### -field Flags

The <a href="/windows/desktop/api/http/ns-http-http_property_flags">HTTP_PROPERTY_FLAGS</a> structure specifying whether the property is present.

### -field State

A member of the <a href="/windows/desktop/api/http/ne-http-http_enabled_state">HTTP_ENABLED_STATE</a> enumeration specifying the whether the configuration object is enabled or disabled.

This can be used to disable a URL Group or Server Session.

## -remarks

When the <b>HttpServerStateProperty</b> is set on a server session or a URL group, the <b>HTTP_STATE_INFO</b> structure must be used. Server Sessions, and URL Groups represent a configuration for a part of the namespace where inheritance is involved.  When traversing the namespace for a request, the HTTP Server API may encounter multiple applicable URL Groups. The property configuration structures must carry information identifying if it is present in a specific URL group.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-2-0-structures">HTTP Server API Version 2.0 Structures</a>



<a href="/windows/desktop/api/http/ne-http-http_server_property">HTTP_SERVER_PROPERTY</a>



<a href="/windows/desktop/api/http/nf-http-httpqueryrequestqueueproperty">HttpQueryRequestQueueProperty</a>



<a href="/windows/desktop/api/http/nf-http-httpqueryserversessionproperty">HttpQueryServerSessionProperty</a>



<a href="/windows/desktop/api/http/nf-http-httpqueryurlgroupproperty">HttpQueryUrlGroupProperty</a>



<a href="/windows/desktop/api/http/nf-http-httpsetrequestqueueproperty">HttpSetRequestQueueProperty</a>



<a href="/windows/desktop/api/http/nf-http-httpsetserversessionproperty">HttpSetServerSessionProperty</a>



<a href="/windows/desktop/api/http/nf-http-httpseturlgroupproperty">HttpSetUrlGroupProperty</a>