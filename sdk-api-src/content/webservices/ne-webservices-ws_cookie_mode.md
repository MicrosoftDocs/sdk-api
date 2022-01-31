---
UID: NE:webservices.__unnamed_enum_26
title: WS_COOKIE_MODE (webservices.h)
description: An enumeration used to specify how to handle HTTP cookies.
helpviewer_keywords: ["WS_AUTO_COOKIE_MODE","WS_COOKIE_MODE","WS_COOKIE_MODE enumeration [Web Services for Windows]","WS_MANUAL_COOKIE_MODE","webservices/WS_AUTO_COOKIE_MODE","webservices/WS_COOKIE_MODE","webservices/WS_MANUAL_COOKIE_MODE","wsw.ws_cookie_mode"]
old-location: wsw\ws_cookie_mode.htm
tech.root: wsw
ms.assetid: d1430120-efaa-4af8-a669-720387c617b2
ms.date: 12/05/2018
ms.keywords: WS_AUTO_COOKIE_MODE, WS_COOKIE_MODE, WS_COOKIE_MODE enumeration [Web Services for Windows], WS_MANUAL_COOKIE_MODE, webservices/WS_AUTO_COOKIE_MODE, webservices/WS_COOKIE_MODE, webservices/WS_MANUAL_COOKIE_MODE, wsw.ws_cookie_mode
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
req.typenames: WS_COOKIE_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_COOKIE_MODE
 - webservices/WS_COOKIE_MODE
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
 - WS_COOKIE_MODE
---

# WS_COOKIE_MODE enumeration


## -description

An enumeration used to specify how to handle HTTP cookies.

## -enum-fields

### -field WS_MANUAL_COOKIE_MODE:1

In this mode, cookies are not processed by the client channel.
                

If a server sends a cookie to the client, the client
                    channel will ignore the cookie (it will not include
                    the cookie value in subsequent requests).
                

An application can use the <a href="/windows/desktop/api/webservices/ns-webservices-ws_http_header_mapping">WS_HTTP_HEADER_MAPPING</a> feature to handle cookies manually, if desired.

### -field WS_AUTO_COOKIE_MODE:2

In this mode, cookies are automatically tracked by
                    the channel.
                

If a server sends a cookie to the client,
                    the channel will automatically track the cookie and
                    will include the cookie in subsequent requests.
