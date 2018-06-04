---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
                

