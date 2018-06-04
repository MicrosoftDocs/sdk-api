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

# WS_RECEIVE_OPTION enumeration


## -description



                Specifies whether a message is required when receiving from a channel.
            


## -enum-fields




### -field WS_RECEIVE_REQUIRED_MESSAGE


                    A message is required to be received.  If the channel does not have
                    any more messages, then the function will fail.
                


### -field WS_RECEIVE_OPTIONAL_MESSAGE


                    The message is not required to be received.  If the channel does not have any more
                    messages, the function will return <b>WS_S_END</b>.
                (See <a href="https://msdn.microsoft.com/96285557-8317-4875-b634-e2eacd605901">Windows Web Services Return Values</a>.)

