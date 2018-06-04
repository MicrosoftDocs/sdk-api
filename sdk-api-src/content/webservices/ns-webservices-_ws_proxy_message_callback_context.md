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

# _WS_PROXY_MESSAGE_CALLBACK_CONTEXT structure


## -description



                Specifies the callback function and state for an application that wishes
                to associate or inspect headers in an input or an output message respectively.
            


                See also, <a href="https://msdn.microsoft.com/d61b6763-9770-4f1d-b16f-c63fc09e8af5">WS_CALL_PROPERTY_SEND_MESSAGE_CONTEXT</a> and  
                <b>WS_CALL_PROPERTY_RECEIVE_MESSAGE_CONTEXT</b>.
            


## -struct-fields




### -field callback


                    application specific callback for handling the message.
                


### -field state


                    Application specific state that would be made available to the callback upon its invocation.
                

