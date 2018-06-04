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

