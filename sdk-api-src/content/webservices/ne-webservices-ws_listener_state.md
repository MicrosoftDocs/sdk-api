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

# WS_LISTENER_STATE enumeration


## -description


The different states that a listener can be in.


## -enum-fields




### -field WS_LISTENER_STATE_CREATED


### -field WS_LISTENER_STATE_OPENING


### -field WS_LISTENER_STATE_OPEN


### -field WS_LISTENER_STATE_FAULTED


### -field WS_LISTENER_STATE_CLOSING


### -field WS_LISTENER_STATE_CLOSED


## -remarks




                The following are the state transitions for a Listener.
            

<img alt="" src="images/ListenerStates.png"/>


                A listener will only move to <b>WS_LISTENER_STATE_FAULTED</b> 
                state if <a href="https://msdn.microsoft.com/894a325b-53ac-4f45-ac24-87ed3a40b03d">WsAbortListener</a> is called.
            


                Note that only the valid state transitions are shown.  Using
                a function not shown for a given state will result in an
                <b>WS_E_INVALID_OPERATION</b> error being returned from
                the function (or crash in the case of <a href="https://msdn.microsoft.com/3a8a4cd3-d98e-467b-bbed-5cbd66f892ed">WsFreeListener</a>).
            See <a href="https://msdn.microsoft.com/96285557-8317-4875-b634-e2eacd605901">Windows Web Services Return Values</a>.



