---
UID: NE:webservices.__unnamed_enum_35
title: WS_LISTENER_STATE (webservices.h)
description: The different states that a listener can be in.
helpviewer_keywords: ["WS_LISTENER_STATE","WS_LISTENER_STATE enumeration [Web Services for Windows]","WS_LISTENER_STATE_CLOSED","WS_LISTENER_STATE_CLOSING","WS_LISTENER_STATE_CREATED","WS_LISTENER_STATE_FAULTED","WS_LISTENER_STATE_OPEN","WS_LISTENER_STATE_OPENING","webservices/WS_LISTENER_STATE","webservices/WS_LISTENER_STATE_CLOSED","webservices/WS_LISTENER_STATE_CLOSING","webservices/WS_LISTENER_STATE_CREATED","webservices/WS_LISTENER_STATE_FAULTED","webservices/WS_LISTENER_STATE_OPEN","webservices/WS_LISTENER_STATE_OPENING","wsw.ws_listener_state"]
old-location: wsw\ws_listener_state.htm
tech.root: wsw
ms.assetid: 275d0d36-f9a1-49a7-af74-e8967dff574a
ms.date: 12/05/2018
ms.keywords: WS_LISTENER_STATE, WS_LISTENER_STATE enumeration [Web Services for Windows], WS_LISTENER_STATE_CLOSED, WS_LISTENER_STATE_CLOSING, WS_LISTENER_STATE_CREATED, WS_LISTENER_STATE_FAULTED, WS_LISTENER_STATE_OPEN, WS_LISTENER_STATE_OPENING, webservices/WS_LISTENER_STATE, webservices/WS_LISTENER_STATE_CLOSED, webservices/WS_LISTENER_STATE_CLOSING, webservices/WS_LISTENER_STATE_CREATED, webservices/WS_LISTENER_STATE_FAULTED, webservices/WS_LISTENER_STATE_OPEN, webservices/WS_LISTENER_STATE_OPENING, wsw.ws_listener_state
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
targetos: Windows
req.typenames: WS_LISTENER_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_LISTENER_STATE
 - webservices/WS_LISTENER_STATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_LISTENER_STATE
---

# WS_LISTENER_STATE enumeration


## -description

The different states that a listener can be in.

## -enum-fields

### -field WS_LISTENER_STATE_CREATED:0

### -field WS_LISTENER_STATE_OPENING:1

### -field WS_LISTENER_STATE_OPEN:2

### -field WS_LISTENER_STATE_FAULTED:3

### -field WS_LISTENER_STATE_CLOSING:4

### -field WS_LISTENER_STATE_CLOSED:5

## -remarks

The following are the state transitions for a Listener.

:::image type="content" source="./images/ListenerStates.png" border="false" alt-text="Diagram showing the possible states of a Listener object and the transitions between them.":::

A listener will only move to <b>WS_LISTENER_STATE_FAULTED</b> 
                state if <a href="/windows/desktop/api/webservices/nf-webservices-wsabortlistener">WsAbortListener</a> is called.
            

Note that only the valid state transitions are shown.  Using
                a function not shown for a given state will result in an
                <b>WS_E_INVALID_OPERATION</b> error being returned from
                the function (or crash in the case of <a href="/windows/desktop/api/webservices/nf-webservices-wsfreelistener">WsFreeListener</a>).
            See <a href="/windows/desktop/wsw/windows-web-services-return-values">Windows Web Services Return Values</a>.
