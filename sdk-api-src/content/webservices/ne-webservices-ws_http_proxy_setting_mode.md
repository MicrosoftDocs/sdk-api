---
UID: NE:webservices.WS_HTTP_PROXY_SETTING_MODE
title: WS_HTTP_PROXY_SETTING_MODE
author: windows-driver-content
description: Proxy setting indicates HTTP proxy setting for the channel with binding WS_HTTP_CHANNEL_BINDING. This is specified as part of WS_CHANNEL_PROPERTY_HTTP_PROXY_SETTING_MODE channel property.
old-location: wsw\ws_http_proxy_setting_mode.htm
old-project: wsw
ms.assetid: 06c2b4e7-59d7-487e-b286-109695124a4d
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: WS_HTTP_PROXY_SETTING_MODE, WS_HTTP_PROXY_SETTING_MODE enumeration [Web Services for Windows], WS_HTTP_PROXY_SETTING_MODE_AUTO, WS_HTTP_PROXY_SETTING_MODE_CUSTOM, WS_HTTP_PROXY_SETTING_MODE_NONE, webservices/WS_HTTP_PROXY_SETTING_MODE, webservices/WS_HTTP_PROXY_SETTING_MODE_AUTO, webservices/WS_HTTP_PROXY_SETTING_MODE_CUSTOM, webservices/WS_HTTP_PROXY_SETTING_MODE_NONE, wsw.ws_http_proxy_setting_mode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: WS_HTTP_PROXY_SETTING_MODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WebServices.h
api_name:
-	WS_HTTP_PROXY_SETTING_MODE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WS_HTTP_PROXY_SETTING_MODE enumeration


## -description



                Proxy setting indicates HTTP proxy setting for the channel with binding <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_HTTP_CHANNEL_BINDING</a>.
                This is specified as part of <a href="https://msdn.microsoft.com/3207c7f0-7f12-4f6b-8ddd-bac9c06ccfbf">WS_CHANNEL_PROPERTY_HTTP_PROXY_SETTING_MODE</a> channel property.
            


## -enum-fields




### -field WS_HTTP_PROXY_SETTING_MODE_AUTO


                    The channel will automatically detect the proxy setting based on the IE configuration for the
                    user at the point the channel is opened. This is the default setting for the <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_HTTP_CHANNEL_BINDING</a>.
                


### -field WS_HTTP_PROXY_SETTING_MODE_NONE


                    No proxy will be used to service the request on the channel.
                


### -field WS_HTTP_PROXY_SETTING_MODE_CUSTOM


                    If an application chooses to explicitly control the HTTP proxy it can use this setting.
                    The <a href="https://msdn.microsoft.com/3207c7f0-7f12-4f6b-8ddd-bac9c06ccfbf">WS_CHANNEL_PROPERTY_CUSTOM_HTTP_PROXY</a> property specifies the custom proxy to be used
                    with the channel and must be set on the channel if this setting is used.
                

