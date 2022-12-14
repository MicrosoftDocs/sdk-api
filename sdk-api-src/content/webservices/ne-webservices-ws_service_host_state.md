---
UID: NE:webservices.__unnamed_enum_95
title: WS_SERVICE_HOST_STATE (webservices.h)
description: The states that a service host can be in.
helpviewer_keywords: ["WS_SERVICE_HOST_STATE","WS_SERVICE_HOST_STATE enumeration [Web Services for Windows]","WS_SERVICE_HOST_STATE_CLOSED","WS_SERVICE_HOST_STATE_CLOSING","WS_SERVICE_HOST_STATE_CREATED","WS_SERVICE_HOST_STATE_FAULTED","WS_SERVICE_HOST_STATE_OPEN","WS_SERVICE_HOST_STATE_OPENING","webservices/WS_SERVICE_HOST_STATE","webservices/WS_SERVICE_HOST_STATE_CLOSED","webservices/WS_SERVICE_HOST_STATE_CLOSING","webservices/WS_SERVICE_HOST_STATE_CREATED","webservices/WS_SERVICE_HOST_STATE_FAULTED","webservices/WS_SERVICE_HOST_STATE_OPEN","webservices/WS_SERVICE_HOST_STATE_OPENING","wsw.ws_service_host_state"]
old-location: wsw\ws_service_host_state.htm
tech.root: wsw
ms.assetid: 99745db7-6e9c-49fd-a97a-4430a80064bb
ms.date: 12/05/2018
ms.keywords: WS_SERVICE_HOST_STATE, WS_SERVICE_HOST_STATE enumeration [Web Services for Windows], WS_SERVICE_HOST_STATE_CLOSED, WS_SERVICE_HOST_STATE_CLOSING, WS_SERVICE_HOST_STATE_CREATED, WS_SERVICE_HOST_STATE_FAULTED, WS_SERVICE_HOST_STATE_OPEN, WS_SERVICE_HOST_STATE_OPENING, webservices/WS_SERVICE_HOST_STATE, webservices/WS_SERVICE_HOST_STATE_CLOSED, webservices/WS_SERVICE_HOST_STATE_CLOSING, webservices/WS_SERVICE_HOST_STATE_CREATED, webservices/WS_SERVICE_HOST_STATE_FAULTED, webservices/WS_SERVICE_HOST_STATE_OPEN, webservices/WS_SERVICE_HOST_STATE_OPENING, wsw.ws_service_host_state
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
req.typenames: WS_SERVICE_HOST_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_SERVICE_HOST_STATE
 - webservices/WS_SERVICE_HOST_STATE
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
 - WS_SERVICE_HOST_STATE
---

# WS_SERVICE_HOST_STATE enumeration


## -description

The states that a service host can be in.

## -enum-fields

### -field WS_SERVICE_HOST_STATE_CREATED:0

### -field WS_SERVICE_HOST_STATE_OPENING:1

### -field WS_SERVICE_HOST_STATE_OPEN:2

### -field WS_SERVICE_HOST_STATE_CLOSING:3

### -field WS_SERVICE_HOST_STATE_CLOSED:4

### -field WS_SERVICE_HOST_STATE_FAULTED:5

## -remarks

The following are the state transitions for a service host.

:::image type="content" source="./images/ServiceHostStates.png" border="false" alt-text="Diagram showing the possible states of a service host object and the transitions between them.":::
