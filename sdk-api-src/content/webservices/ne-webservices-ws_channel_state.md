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

# WS_CHANNEL_STATE enumeration


## -description


The different states that a channel can be in.


## -enum-fields




### -field WS_CHANNEL_STATE_CREATED


### -field WS_CHANNEL_STATE_OPENING


### -field WS_CHANNEL_STATE_ACCEPTING


### -field WS_CHANNEL_STATE_OPEN


### -field WS_CHANNEL_STATE_FAULTED


### -field WS_CHANNEL_STATE_CLOSING


### -field WS_CHANNEL_STATE_CLOSED


## -remarks




                The following are the state transitions for a channel.
            

<img alt="" src="images/ChannelStates.png"/>


                A channel may move to the <b>WS_CHANNEL_STATE_FAULTED</b> 
                state even if <a href="https://msdn.microsoft.com/67af85d7-db75-4e26-a7cc-8115ac3f2d59">WsAbortChannel</a> was never called.
                This will only occur if the channel can no longer be used.
            


                Note that only the valid state transitions are shown.  Using
                a function not shown for a given state will result in an
                <b>WS_E_INVALID_OPERATION</b> error being returned from
                the function (or crash in the case of <a href="https://msdn.microsoft.com/74e36d19-c6db-4bba-90e3-88a48b6a1fb5">WsFreeChannel</a>).
            For information on error codes, see<a href="https://msdn.microsoft.com/96285557-8317-4875-b634-e2eacd605901">Windows Web Services Return Values</a>.



