---
UID: NE:webservices.WS_CHANNEL_BINDING
title: WS_CHANNEL_BINDING
author: windows-driver-content
description: Indicates the protocol stack to use for the channel.
old-location: wsw\ws_channel_binding.htm
old-project: wsw
ms.assetid: 554cc239-feab-4262-9821-6478a3d93ffc
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: WS_CHANNEL_BINDING, WS_CHANNEL_BINDING enumeration [Web Services for Windows], WS_CUSTOM_CHANNEL_BINDING, WS_HTTP_CHANNEL_BINDING, WS_NAMEDPIPE_CHANNEL_BINDING, WS_TCP_CHANNEL_BINDING, WS_UDP_CHANNEL_BINDING, webservices/WS_CHANNEL_BINDING, webservices/WS_CUSTOM_CHANNEL_BINDING, webservices/WS_HTTP_CHANNEL_BINDING, webservices/WS_NAMEDPIPE_CHANNEL_BINDING, webservices/WS_TCP_CHANNEL_BINDING, webservices/WS_UDP_CHANNEL_BINDING, wsw.ws_channel_binding
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WS_CHANNEL_BINDING
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WebServices.h
api_name:
-	WS_CHANNEL_BINDING
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WS_CHANNEL_BINDING enumeration


## -description


Indicates the protocol stack to use for the channel.
            


## -enum-fields




### -field WS_HTTP_CHANNEL_BINDING


                    SOAP over HTTP.
                


### -field WS_TCP_CHANNEL_BINDING


                    SOAP over TCP.
                


### -field WS_UDP_CHANNEL_BINDING


                    SOAP over UDP.
                


### -field WS_CUSTOM_CHANNEL_BINDING

A custom channel or listen implementation. For more information, see <a href="https://msdn.microsoft.com/8df774fd-7cfc-4006-84ad-b81737770b6e">WS_CUSTOM_CHANNEL_CALLBACKS</a> and <a href="https://msdn.microsoft.com/b0be530f-5eff-4daa-90be-f9be648dfad7">WS_CUSTOM_LISTENER_CALLBACKS</a>.


### -field WS_NAMEDPIPE_CHANNEL_BINDING

Windows 8 or later:
                    SOAP over named pipes.

