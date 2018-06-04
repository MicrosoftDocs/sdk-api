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

# WsFreeListener function


## -description


Releases the memory resource associated with a Listener object.
            The Listener state represented in <a href="https://msdn.microsoft.com/275d0d36-f9a1-49a7-af74-e8967dff574a">WS_LISTENER_STATE</a> must be set to either <b>WS_LISTENER_STATE_CREATED</b> 
                or <b>WS_LISTENER_STATE_CLOSED</b> to be released.
            If a Listener has been successfully opened, then it must be closed 
                using <a href="https://msdn.microsoft.com/6023595a-ac52-4619-a824-df49da887fc5">WsCloseListener</a> before it is released.


## -parameters




### -param listener [in]


                    A pointer to the <b>Listener</b> object to release.  The pointer must reference a valid <a href="https://msdn.microsoft.com/2e771c56-4a07-4c8e-92c1-ffcbf74cd1aa">WS_LISTENER</a> returned
                    by <a href="https://msdn.microsoft.com/2e592fd2-cf88-4f87-a71b-1c3416917fa7">WsCreateListener</a>.  The referenced value may not be <b>NULL</b>.
                


## -returns



This function does not return a value.



