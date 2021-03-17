---
UID: NE:http._HTTP_ENABLED_STATE
title: HTTP_ENABLED_STATE (http.h)
description: Defines the state of a request queue, server session, or URL Group.
helpviewer_keywords: ["*PHTTP_ENABLED_STATE","*PHTTP_ENABLED_STATE enumeration [HTTP]","HTTP_ENABLED_STATE","HTTP_ENABLED_STATE enumeration [HTTP]","HttpEnabledStateActive","HttpEnabledStateInactive","http.http_enabled_state","http/*PHTTP_ENABLED_STATE","http/HTTP_ENABLED_STATE","http/HttpEnabledStateActive","http/HttpEnabledStateInactive"]
old-location: http\http_enabled_state.htm
tech.root: http
ms.assetid: 15e27788-2d1a-4818-b31f-2faf649e15b2
ms.date: 12/05/2018
ms.keywords: '*PHTTP_ENABLED_STATE, *PHTTP_ENABLED_STATE enumeration [HTTP], HTTP_ENABLED_STATE, HTTP_ENABLED_STATE enumeration [HTTP], HttpEnabledStateActive, HttpEnabledStateInactive, http.http_enabled_state, http/*PHTTP_ENABLED_STATE, http/HTTP_ENABLED_STATE, http/HttpEnabledStateActive, http/HttpEnabledStateInactive'
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
req.typenames: HTTP_ENABLED_STATE, *PHTTP_ENABLED_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_ENABLED_STATE
 - http/_HTTP_ENABLED_STATE
 - PHTTP_ENABLED_STATE
 - http/PHTTP_ENABLED_STATE
 - HTTP_ENABLED_STATE
 - http/HTTP_ENABLED_STATE
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
 - HTTP_ENABLED_STATE
---

# HTTP_ENABLED_STATE enumeration


## -description

The <b>HTTP_ENABLED_STATE</b> enumeration defines the state of a request queue, server session, or URL Group.

This enumeration is used in the <a href="/windows/desktop/api/http/ns-http-http_state_info">HTTP_STATE_INFO</a> struct

## -enum-fields

### -field HttpEnabledStateActive

The HTTP Server API object is enabled.

### -field HttpEnabledStateInactive

The HTTP Server API object is disabled.

## -remarks

 The default state of a request queue is enabled. Typically this enumeration is used to temporarily disable a request queue.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-2-0-enumeration-types">HTTP Server API Version 2.0 Enumeration Types</a>



<a href="/windows/desktop/api/http/ns-http-http_state_info">HTTP_STATE_INFO</a>