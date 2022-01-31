---
UID: NE:webservices.__unnamed_enum_98
title: WS_CALL_PROPERTY_ID (webservices.h)
description: Optional parameters for configuring a call on a client side service operation.
helpviewer_keywords: ["WS_CALL_PROPERTY_CALL_ID","WS_CALL_PROPERTY_CHECK_MUST_UNDERSTAND","WS_CALL_PROPERTY_ID","WS_CALL_PROPERTY_ID enumeration [Web Services for Windows]","WS_CALL_PROPERTY_RECEIVE_MESSAGE_CONTEXT","WS_CALL_PROPERTY_SEND_MESSAGE_CONTEXT","webservices/WS_CALL_PROPERTY_CALL_ID","webservices/WS_CALL_PROPERTY_CHECK_MUST_UNDERSTAND","webservices/WS_CALL_PROPERTY_ID","webservices/WS_CALL_PROPERTY_RECEIVE_MESSAGE_CONTEXT","webservices/WS_CALL_PROPERTY_SEND_MESSAGE_CONTEXT","wsw.ws_call_property_id"]
old-location: wsw\ws_call_property_id.htm
tech.root: wsw
ms.assetid: d61b6763-9770-4f1d-b16f-c63fc09e8af5
ms.date: 12/05/2018
ms.keywords: WS_CALL_PROPERTY_CALL_ID, WS_CALL_PROPERTY_CHECK_MUST_UNDERSTAND, WS_CALL_PROPERTY_ID, WS_CALL_PROPERTY_ID enumeration [Web Services for Windows], WS_CALL_PROPERTY_RECEIVE_MESSAGE_CONTEXT, WS_CALL_PROPERTY_SEND_MESSAGE_CONTEXT, webservices/WS_CALL_PROPERTY_CALL_ID, webservices/WS_CALL_PROPERTY_CHECK_MUST_UNDERSTAND, webservices/WS_CALL_PROPERTY_ID, webservices/WS_CALL_PROPERTY_RECEIVE_MESSAGE_CONTEXT, webservices/WS_CALL_PROPERTY_SEND_MESSAGE_CONTEXT, wsw.ws_call_property_id
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.typenames: WS_CALL_PROPERTY_ID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_CALL_PROPERTY_ID
 - webservices/WS_CALL_PROPERTY_ID
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
 - WS_CALL_PROPERTY_ID
---

# WS_CALL_PROPERTY_ID enumeration


## -description

Optional parameters for configuring a call on a client side service operation.

## -enum-fields

### -field WS_CALL_PROPERTY_CHECK_MUST_UNDERSTAND:0

An application can suppress or enable must understand header processing 
                    on the proxy using this setting. This is <b>TRUE</b> by default.

### -field WS_CALL_PROPERTY_SEND_MESSAGE_CONTEXT:1

Enables an application to put headers into the input message for a given call.

### -field WS_CALL_PROPERTY_RECEIVE_MESSAGE_CONTEXT:2

Enables an application to extract headers from the output message for a given call.

### -field WS_CALL_PROPERTY_CALL_ID:3

On a <a href="/windows/desktop/wsw/service-operation">service operation</a> an application can use the call id property to uniquely identify 
                    a service operation function all on a channel. This ID can be passed on to <a href="/windows/desktop/api/webservices/nf-webservices-wsabandoncall">WsAbandonCall</a> along with the
                    service proxy to abandon the call.
                

For more information about abandoning calls see <a href="/windows/desktop/wsw/client-side-service-operations">service operation</a>.
