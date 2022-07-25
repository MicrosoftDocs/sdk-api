---
UID: NE:webservices.__unnamed_enum_27
title: WS_OPERATION_CONTEXT_PROPERTY_ID (webservices.h)
description: The properties available on the Context. Not all properties may be available at a given point on a context. All context properties are available through WsGetOperationContextProperty.
helpviewer_keywords: ["WS_OPERATION_CONTEXT_PROPERTY_CHANNEL","WS_OPERATION_CONTEXT_PROPERTY_CHANNEL_USER_STATE","WS_OPERATION_CONTEXT_PROPERTY_CONTRACT_DESCRIPTION","WS_OPERATION_CONTEXT_PROPERTY_HEAP","WS_OPERATION_CONTEXT_PROPERTY_HOST_USER_STATE","WS_OPERATION_CONTEXT_PROPERTY_ID","WS_OPERATION_CONTEXT_PROPERTY_ID enumeration [Web Services for Windows]","WS_OPERATION_CONTEXT_PROPERTY_INPUT_MESSAGE","WS_OPERATION_CONTEXT_PROPERTY_OUTPUT_MESSAGE","webservices/WS_OPERATION_CONTEXT_PROPERTY_CHANNEL","webservices/WS_OPERATION_CONTEXT_PROPERTY_CHANNEL_USER_STATE","webservices/WS_OPERATION_CONTEXT_PROPERTY_CONTRACT_DESCRIPTION","webservices/WS_OPERATION_CONTEXT_PROPERTY_HEAP","webservices/WS_OPERATION_CONTEXT_PROPERTY_HOST_USER_STATE","webservices/WS_OPERATION_CONTEXT_PROPERTY_ID","webservices/WS_OPERATION_CONTEXT_PROPERTY_INPUT_MESSAGE","webservices/WS_OPERATION_CONTEXT_PROPERTY_OUTPUT_MESSAGE","wsw.ws_operation_context_property_id"]
old-location: wsw\ws_operation_context_property_id.htm
tech.root: wsw
ms.assetid: 71f7d0fe-c120-4667-93de-a0dfb94fccc1
ms.date: 12/05/2018
ms.keywords: WS_OPERATION_CONTEXT_PROPERTY_CHANNEL, WS_OPERATION_CONTEXT_PROPERTY_CHANNEL_USER_STATE, WS_OPERATION_CONTEXT_PROPERTY_CONTRACT_DESCRIPTION, WS_OPERATION_CONTEXT_PROPERTY_HEAP, WS_OPERATION_CONTEXT_PROPERTY_HOST_USER_STATE, WS_OPERATION_CONTEXT_PROPERTY_ID, WS_OPERATION_CONTEXT_PROPERTY_ID enumeration [Web Services for Windows], WS_OPERATION_CONTEXT_PROPERTY_INPUT_MESSAGE, WS_OPERATION_CONTEXT_PROPERTY_OUTPUT_MESSAGE, webservices/WS_OPERATION_CONTEXT_PROPERTY_CHANNEL, webservices/WS_OPERATION_CONTEXT_PROPERTY_CHANNEL_USER_STATE, webservices/WS_OPERATION_CONTEXT_PROPERTY_CONTRACT_DESCRIPTION, webservices/WS_OPERATION_CONTEXT_PROPERTY_HEAP, webservices/WS_OPERATION_CONTEXT_PROPERTY_HOST_USER_STATE, webservices/WS_OPERATION_CONTEXT_PROPERTY_ID, webservices/WS_OPERATION_CONTEXT_PROPERTY_INPUT_MESSAGE, webservices/WS_OPERATION_CONTEXT_PROPERTY_OUTPUT_MESSAGE, wsw.ws_operation_context_property_id
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
req.typenames: WS_OPERATION_CONTEXT_PROPERTY_ID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_OPERATION_CONTEXT_PROPERTY_ID
 - webservices/WS_OPERATION_CONTEXT_PROPERTY_ID
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
 - WS_OPERATION_CONTEXT_PROPERTY_ID
---

# WS_OPERATION_CONTEXT_PROPERTY_ID enumeration


## -description

The properties available on the Context. Not all properties may be available
                at a given point on a context. All context properties are available through <a href="/windows/desktop/api/webservices/nf-webservices-wsgetoperationcontextproperty">WsGetOperationContextProperty</a>.

## -enum-fields

### -field WS_OPERATION_CONTEXT_PROPERTY_CHANNEL:0

This value is a handle to the underlying channel. This property is available to service operations ,
                    to the <a href="/windows/desktop/api/webservices/nc-webservices-ws_service_message_receive_callback">WS_SERVICE_MESSAGE_RECEIVE_CALLBACK</a>, <a href="/windows/desktop/api/webservices/nc-webservices-ws_service_accept_channel_callback">WS_SERVICE_ACCEPT_CHANNEL_CALLBACK</a> and 
                    <a href="/windows/desktop/api/webservices/nc-webservices-ws_service_close_channel_callback">WS_SERVICE_CLOSE_CHANNEL_CALLBACK</a>.

### -field WS_OPERATION_CONTEXT_PROPERTY_CONTRACT_DESCRIPTION:1

The value represents the contract description. This property is available to service operations ,
                    to the <a href="/windows/desktop/api/webservices/nc-webservices-ws_service_message_receive_callback">WS_SERVICE_MESSAGE_RECEIVE_CALLBACK</a>, <a href="/windows/desktop/api/webservices/nc-webservices-ws_service_accept_channel_callback">WS_SERVICE_ACCEPT_CHANNEL_CALLBACK</a> and 
                    <a href="/windows/desktop/api/webservices/nc-webservices-ws_service_close_channel_callback">WS_SERVICE_CLOSE_CHANNEL_CALLBACK</a>.

### -field WS_OPERATION_CONTEXT_PROPERTY_HOST_USER_STATE:2

The value is a pointer to the host state specified on the <a href="/windows/desktop/wsw/service-host">service host</a> as the 
                    <a href="/windows/desktop/api/webservices/ne-webservices-ws_service_property_id">WS_SERVICE_PROPERTY_HOST_USER_STATE</a> service property. This property is available to 
                     service operations  and to the <a href="/windows/desktop/api/webservices/nc-webservices-ws_service_message_receive_callback">WS_SERVICE_MESSAGE_RECEIVE_CALLBACK</a>.

### -field WS_OPERATION_CONTEXT_PROPERTY_CHANNEL_USER_STATE:3

The value is a pointer to the channel state specified through <a href="/windows/desktop/api/webservices/nc-webservices-ws_service_accept_channel_callback">WS_SERVICE_ACCEPT_CHANNEL_CALLBACK</a>. This property is 
                    available to  service operations and to the <a href="/windows/desktop/api/webservices/nc-webservices-ws_service_message_receive_callback">WS_SERVICE_MESSAGE_RECEIVE_CALLBACK</a>.

### -field WS_OPERATION_CONTEXT_PROPERTY_INPUT_MESSAGE:4

The value is a pointer to the underlying input message. This property is available to service operations and to the 
                    <a href="/windows/desktop/api/webservices/nc-webservices-ws_service_message_receive_callback">WS_SERVICE_MESSAGE_RECEIVE_CALLBACK</a>.

### -field WS_OPERATION_CONTEXT_PROPERTY_OUTPUT_MESSAGE:5

The value is a pointer to the underlying output message. This property is available only to service operations.

### -field WS_OPERATION_CONTEXT_PROPERTY_HEAP:6

The value is a pointer to the WS_HEAP. This property is available to a service operation. Please see the memory management section in 
                    service operations for usage.

### -field WS_OPERATION_CONTEXT_PROPERTY_LISTENER:7

### -field WS_OPERATION_CONTEXT_PROPERTY_ENDPOINT_ADDRESS:8
