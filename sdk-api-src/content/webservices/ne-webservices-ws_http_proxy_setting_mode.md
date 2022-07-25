---
UID: NE:webservices.__unnamed_enum_21
title: WS_HTTP_PROXY_SETTING_MODE (webservices.h)
description: Proxy setting indicates HTTP proxy setting for the channel with binding WS_HTTP_CHANNEL_BINDING. This is specified as part of WS_CHANNEL_PROPERTY_HTTP_PROXY_SETTING_MODE channel property.
helpviewer_keywords: ["WS_HTTP_PROXY_SETTING_MODE","WS_HTTP_PROXY_SETTING_MODE enumeration [Web Services for Windows]","WS_HTTP_PROXY_SETTING_MODE_AUTO","WS_HTTP_PROXY_SETTING_MODE_CUSTOM","WS_HTTP_PROXY_SETTING_MODE_NONE","webservices/WS_HTTP_PROXY_SETTING_MODE","webservices/WS_HTTP_PROXY_SETTING_MODE_AUTO","webservices/WS_HTTP_PROXY_SETTING_MODE_CUSTOM","webservices/WS_HTTP_PROXY_SETTING_MODE_NONE","wsw.ws_http_proxy_setting_mode"]
old-location: wsw\ws_http_proxy_setting_mode.htm
tech.root: wsw
ms.assetid: 06c2b4e7-59d7-487e-b286-109695124a4d
ms.date: 12/05/2018
ms.keywords: WS_HTTP_PROXY_SETTING_MODE, WS_HTTP_PROXY_SETTING_MODE enumeration [Web Services for Windows], WS_HTTP_PROXY_SETTING_MODE_AUTO, WS_HTTP_PROXY_SETTING_MODE_CUSTOM, WS_HTTP_PROXY_SETTING_MODE_NONE, webservices/WS_HTTP_PROXY_SETTING_MODE, webservices/WS_HTTP_PROXY_SETTING_MODE_AUTO, webservices/WS_HTTP_PROXY_SETTING_MODE_CUSTOM, webservices/WS_HTTP_PROXY_SETTING_MODE_NONE, wsw.ws_http_proxy_setting_mode
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
req.typenames: WS_HTTP_PROXY_SETTING_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_HTTP_PROXY_SETTING_MODE
 - webservices/WS_HTTP_PROXY_SETTING_MODE
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
 - WS_HTTP_PROXY_SETTING_MODE
---

# WS_HTTP_PROXY_SETTING_MODE enumeration


## -description

Proxy setting indicates HTTP proxy setting for the channel with binding <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_binding">WS_HTTP_CHANNEL_BINDING</a>.
                This is specified as part of <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_property_id">WS_CHANNEL_PROPERTY_HTTP_PROXY_SETTING_MODE</a> channel property.

## -enum-fields

### -field WS_HTTP_PROXY_SETTING_MODE_AUTO:0x1

The channel will automatically detect the proxy setting based on the IE configuration for the
                    user at the point the channel is opened. This is the default setting for the <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_binding">WS_HTTP_CHANNEL_BINDING</a>.

### -field WS_HTTP_PROXY_SETTING_MODE_NONE:0x2

No proxy will be used to service the request on the channel.

### -field WS_HTTP_PROXY_SETTING_MODE_CUSTOM:0x3

If an application chooses to explicitly control the HTTP proxy it can use this setting.
                    The <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_property_id">WS_CHANNEL_PROPERTY_CUSTOM_HTTP_PROXY</a> property specifies the custom proxy to be used
                    with the channel and must be set on the channel if this setting is used.
