---
UID: NE:webservices.__unnamed_enum_49
title: WS_HTTP_HEADER_AUTH_TARGET (webservices.h)
description: Defines the target for the HTTP header authentication security binding.
helpviewer_keywords: ["WS_HTTP_HEADER_AUTH_TARGET","WS_HTTP_HEADER_AUTH_TARGET enumeration [Web Services for Windows]","WS_HTTP_HEADER_AUTH_TARGET_PROXY","WS_HTTP_HEADER_AUTH_TARGET_SERVICE","webservices/WS_HTTP_HEADER_AUTH_TARGET","webservices/WS_HTTP_HEADER_AUTH_TARGET_PROXY","webservices/WS_HTTP_HEADER_AUTH_TARGET_SERVICE","wsw.ws_http_header_auth_target"]
old-location: wsw\ws_http_header_auth_target.htm
tech.root: wsw
ms.assetid: d8e9b1b9-70b7-41b3-bbf0-7cd04ebabf55
ms.date: 12/05/2018
ms.keywords: WS_HTTP_HEADER_AUTH_TARGET, WS_HTTP_HEADER_AUTH_TARGET enumeration [Web Services for Windows], WS_HTTP_HEADER_AUTH_TARGET_PROXY, WS_HTTP_HEADER_AUTH_TARGET_SERVICE, webservices/WS_HTTP_HEADER_AUTH_TARGET, webservices/WS_HTTP_HEADER_AUTH_TARGET_PROXY, webservices/WS_HTTP_HEADER_AUTH_TARGET_SERVICE, wsw.ws_http_header_auth_target
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: WS_HTTP_HEADER_AUTH_TARGET
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_HTTP_HEADER_AUTH_TARGET
 - webservices/WS_HTTP_HEADER_AUTH_TARGET
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_HTTP_HEADER_AUTH_TARGET
---

# WS_HTTP_HEADER_AUTH_TARGET enumeration


## -description

Defines the target for the HTTP header authentication security binding.

## -enum-fields

### -field WS_HTTP_HEADER_AUTH_TARGET_SERVICE:1

Indicates that the <a href="/windows/desktop/api/webservices/ns-webservices-ws_http_header_auth_security_binding">WS_HTTP_HEADER_AUTH_SECURITY_BINDING</a> containing
this setting authenticates to the server.

### -field WS_HTTP_HEADER_AUTH_TARGET_PROXY:2

Indicates that the <a href="/windows/desktop/api/webservices/ns-webservices-ws_http_header_auth_security_binding">WS_HTTP_HEADER_AUTH_SECURITY_BINDING</a> containing
this setting authenticates to the proxy.
