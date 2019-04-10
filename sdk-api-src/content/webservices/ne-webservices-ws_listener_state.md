---
UID: NE:webservices.__unnamed_enum_35
title: WS_LISTENER_STATE (webservices.h)
author: windows-sdk-content
description: The different states that a listener can be in.
old-location: wsw\ws_listener_state.htm
tech.root: wsw
ms.assetid: 275d0d36-f9a1-49a7-af74-e8967dff574a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WS_LISTENER_STATE, WS_LISTENER_STATE enumeration [Web Services for Windows], WS_LISTENER_STATE_CLOSED, WS_LISTENER_STATE_CLOSING, WS_LISTENER_STATE_CREATED, WS_LISTENER_STATE_FAULTED, WS_LISTENER_STATE_OPEN, WS_LISTENER_STATE_OPENING, webservices/WS_LISTENER_STATE, webservices/WS_LISTENER_STATE_CLOSED, webservices/WS_LISTENER_STATE_CLOSING, webservices/WS_LISTENER_STATE_CREATED, webservices/WS_LISTENER_STATE_FAULTED, webservices/WS_LISTENER_STATE_OPEN, webservices/WS_LISTENER_STATE_OPENING, wsw.ws_listener_state
ms.topic: enum
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_LISTENER_STATE
product: Windows
targetos: Windows
req.typenames: WS_LISTENER_STATE
req.redist: 
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
            

<img alt="" src="./images/ListenerStates.png"/>

A listener will only move to <b>WS_LISTENER_STATE_FAULTED</b> 
                state if <a href="https://msdn.microsoft.com/894a325b-53ac-4f45-ac24-87ed3a40b03d">WsAbortListener</a> is called.
            

Note that only the valid state transitions are shown.  Using
                a function not shown for a given state will result in an
                <b>WS_E_INVALID_OPERATION</b> error being returned from
                the function (or crash in the case of <a href="https://msdn.microsoft.com/3a8a4cd3-d98e-467b-bbed-5cbd66f892ed">WsFreeListener</a>).
            See <a href="https://msdn.microsoft.com/96285557-8317-4875-b634-e2eacd605901">Windows Web Services Return Values</a>.



