---
UID: NE:webservices.__unnamed_enum_16
title: WS_CHANNEL_STATE (webservices.h)
description: The different states that a channel can be in.
helpviewer_keywords: ["WS_CHANNEL_STATE","WS_CHANNEL_STATE enumeration [Web Services for Windows]","WS_CHANNEL_STATE_ACCEPTING","WS_CHANNEL_STATE_CLOSED","WS_CHANNEL_STATE_CLOSING","WS_CHANNEL_STATE_CREATED","WS_CHANNEL_STATE_FAULTED","WS_CHANNEL_STATE_OPEN","WS_CHANNEL_STATE_OPENING","webservices/WS_CHANNEL_STATE","webservices/WS_CHANNEL_STATE_ACCEPTING","webservices/WS_CHANNEL_STATE_CLOSED","webservices/WS_CHANNEL_STATE_CLOSING","webservices/WS_CHANNEL_STATE_CREATED","webservices/WS_CHANNEL_STATE_FAULTED","webservices/WS_CHANNEL_STATE_OPEN","webservices/WS_CHANNEL_STATE_OPENING","wsw.ws_channel_state"]
old-location: wsw\ws_channel_state.htm
tech.root: wsw
ms.assetid: 3a7f5bbd-e484-4a7e-8e5d-df229a7227a5
ms.date: 12/05/2018
ms.keywords: WS_CHANNEL_STATE, WS_CHANNEL_STATE enumeration [Web Services for Windows], WS_CHANNEL_STATE_ACCEPTING, WS_CHANNEL_STATE_CLOSED, WS_CHANNEL_STATE_CLOSING, WS_CHANNEL_STATE_CREATED, WS_CHANNEL_STATE_FAULTED, WS_CHANNEL_STATE_OPEN, WS_CHANNEL_STATE_OPENING, webservices/WS_CHANNEL_STATE, webservices/WS_CHANNEL_STATE_ACCEPTING, webservices/WS_CHANNEL_STATE_CLOSED, webservices/WS_CHANNEL_STATE_CLOSING, webservices/WS_CHANNEL_STATE_CREATED, webservices/WS_CHANNEL_STATE_FAULTED, webservices/WS_CHANNEL_STATE_OPEN, webservices/WS_CHANNEL_STATE_OPENING, wsw.ws_channel_state
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
req.typenames: WS_CHANNEL_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_CHANNEL_STATE
 - webservices/WS_CHANNEL_STATE
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
 - WS_CHANNEL_STATE
---

# WS_CHANNEL_STATE enumeration


## -description

The different states that a channel can be in.

## -enum-fields

### -field WS_CHANNEL_STATE_CREATED:0

### -field WS_CHANNEL_STATE_OPENING:1

### -field WS_CHANNEL_STATE_ACCEPTING:2

### -field WS_CHANNEL_STATE_OPEN:3

### -field WS_CHANNEL_STATE_FAULTED:4

### -field WS_CHANNEL_STATE_CLOSING:5

### -field WS_CHANNEL_STATE_CLOSED:6

## -remarks

The following are the state transitions for a channel.
            

:::image type="content" source="./images/ChannelStates.png" border="false" alt-text="Diagram of the state transitions for a Channel object. A second diagram shows the Sub-states for the Channel's Open state.":::

A channel may move to the <b>WS_CHANNEL_STATE_FAULTED</b> 
                state even if <a href="/windows/desktop/api/webservices/nf-webservices-wsabortchannel">WsAbortChannel</a> was never called.
                This will only occur if the channel can no longer be used.
            

Note that only the valid state transitions are shown.  Using
                a function not shown for a given state will result in an
                <b>WS_E_INVALID_OPERATION</b> error being returned from
                the function (or crash in the case of <a href="/windows/desktop/api/webservices/nf-webservices-wsfreechannel">WsFreeChannel</a>).
            For information on error codes, see<a href="/windows/desktop/wsw/windows-web-services-return-values">Windows Web Services Return Values</a>.
