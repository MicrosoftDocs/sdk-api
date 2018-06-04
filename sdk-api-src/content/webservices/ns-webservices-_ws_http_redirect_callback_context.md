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

# _WS_HTTP_REDIRECT_CALLBACK_CONTEXT structure


## -description



                Specifies the callback function and state for controlling the HTTP auto redirection behavior.
            


                See also, <b>WS_HTTP_REDIRECT_CALLBACK_CONTEXT</b> 
                and <a href="https://msdn.microsoft.com/3207c7f0-7f12-4f6b-8ddd-bac9c06ccfbf">WS_CHANNEL_PROPERTY_HTTP_REDIRECT_CALLBACK_CONTEXT</a>.
            


## -struct-fields




### -field callback


                    Application specific callback for controlling HTTP auto redirections.
                


### -field state


                    Application specific state that would be made available to the callback upon its invocation.
                

