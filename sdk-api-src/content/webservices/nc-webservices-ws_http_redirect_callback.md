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

# WS_HTTP_REDIRECT_CALLBACK callback function


## -description


Invoked when a message is about to be automatically 
                redirected to another service utilizing HTTP auto redirect functionality 
                as described in RFC2616. If the redirection should not be allowed, this 
                callback should return S_FALSE or an error value. Otherwise the auto 
                HTTP redirection will proceed. 
            


## -parameters




### -param *state [in]


                    The 'state' as specified as part of <a href="https://msdn.microsoft.com/2348fcdb-2f76-4a30-91c4-ed7d63012da1">WS_HTTP_REDIRECT_CALLBACK_CONTEXT</a> 'state' field.
                


### -param *originalUrl [in]


                    The original endpoint URL that the message was sent to.
                


### -param *newUrl [in]


                    The endpoint URL that the message is about to be forwarded to.
                


## -returns



This callback function does not return a value.




## -remarks




                The parameters supplied during this callback are valid only for the 
                duration of the callback.
            


                The callback implementation should avoid lengthy computation or 
                lengthy blocking calls so that it can return to the caller quickly.
            



