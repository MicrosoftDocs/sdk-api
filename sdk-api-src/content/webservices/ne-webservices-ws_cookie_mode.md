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

# WS_COOKIE_MODE enumeration


## -description



                An enumeration used to specify how to handle HTTP cookies.
            


## -enum-fields




### -field WS_MANUAL_COOKIE_MODE


                    In this mode, cookies are not processed by the client channel.
                


                    If a server sends a cookie to the client, the client
                    channel will ignore the cookie (it will not include
                    the cookie value in subsequent requests).
                


                    An application can use the <a href="https://msdn.microsoft.com/bca1f244-4692-42bb-bbd7-c96647038a06">WS_HTTP_HEADER_MAPPING</a>
                    feature to handle cookies manually, if desired.
                


### -field WS_AUTO_COOKIE_MODE


                    In this mode, cookies are automatically tracked by
                    the channel.
                


                    If a server sends a cookie to the client,
                    the channel will automatically track the cookie and
                    will include the cookie in subsequent requests.
                

