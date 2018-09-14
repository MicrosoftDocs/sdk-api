---
UID: NE:webservices.WS_OPERATION_CONTEXT_PROPERTY_ID
title: WS_OPERATION_CONTEXT_PROPERTY_ID
author: windows-sdk-content
description: The properties available on the Context. Not all properties may be available at a given point on a context. All context properties are available through WsGetOperationContextProperty.
old-location: wsw\ws_operation_context_property_id.htm
tech.root: wsw
ms.assetid: 71f7d0fe-c120-4667-93de-a0dfb94fccc1
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: WS_OPERATION_CONTEXT_PROPERTY_CHANNEL, WS_OPERATION_CONTEXT_PROPERTY_CHANNEL_USER_STATE, WS_OPERATION_CONTEXT_PROPERTY_CONTRACT_DESCRIPTION, WS_OPERATION_CONTEXT_PROPERTY_HEAP, WS_OPERATION_CONTEXT_PROPERTY_HOST_USER_STATE, WS_OPERATION_CONTEXT_PROPERTY_ID, WS_OPERATION_CONTEXT_PROPERTY_ID enumeration [Web Services for Windows], WS_OPERATION_CONTEXT_PROPERTY_INPUT_MESSAGE, WS_OPERATION_CONTEXT_PROPERTY_OUTPUT_MESSAGE, webservices/WS_OPERATION_CONTEXT_PROPERTY_CHANNEL, webservices/WS_OPERATION_CONTEXT_PROPERTY_CHANNEL_USER_STATE, webservices/WS_OPERATION_CONTEXT_PROPERTY_CONTRACT_DESCRIPTION, webservices/WS_OPERATION_CONTEXT_PROPERTY_HEAP, webservices/WS_OPERATION_CONTEXT_PROPERTY_HOST_USER_STATE, webservices/WS_OPERATION_CONTEXT_PROPERTY_ID, webservices/WS_OPERATION_CONTEXT_PROPERTY_INPUT_MESSAGE, webservices/WS_OPERATION_CONTEXT_PROPERTY_OUTPUT_MESSAGE, wsw.ws_operation_context_property_id
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_OPERATION_CONTEXT_PROPERTY_ID
product: Windows
targetos: Windows
req.typenames: WS_OPERATION_CONTEXT_PROPERTY_ID
req.redist: 
---

# WS_OPERATION_CONTEXT_PROPERTY_ID enumeration


## -description


The properties available on the Context. Not all properties may be available
                at a given point on a context. All context properties are available through <a href="https://msdn.microsoft.com/9ab843ff-8f2c-424e-8bb9-ba71f9355728">WsGetOperationContextProperty</a>. 
            


## -enum-fields




### -field WS_OPERATION_CONTEXT_PROPERTY_CHANNEL

This value is a handle to the underlying channel. This property is available to service operations ,
                    to the <a href="https://msdn.microsoft.com/2fcd8905-7002-41b8-b947-14d53c889c21">WS_SERVICE_MESSAGE_RECEIVE_CALLBACK</a>, <a href="https://msdn.microsoft.com/473af4be-d193-42a5-82ff-359b50a7bc58">WS_SERVICE_ACCEPT_CHANNEL_CALLBACK</a> and 
                    <a href="https://msdn.microsoft.com/e2860015-219b-46be-921d-7ced0d95fc60">WS_SERVICE_CLOSE_CHANNEL_CALLBACK</a>.
                


### -field WS_OPERATION_CONTEXT_PROPERTY_CONTRACT_DESCRIPTION

The value represents the contract description. This property is available to service operations ,
                    to the <a href="https://msdn.microsoft.com/2fcd8905-7002-41b8-b947-14d53c889c21">WS_SERVICE_MESSAGE_RECEIVE_CALLBACK</a>, <a href="https://msdn.microsoft.com/473af4be-d193-42a5-82ff-359b50a7bc58">WS_SERVICE_ACCEPT_CHANNEL_CALLBACK</a> and 
                    <a href="https://msdn.microsoft.com/e2860015-219b-46be-921d-7ced0d95fc60">WS_SERVICE_CLOSE_CHANNEL_CALLBACK</a>.
                


### -field WS_OPERATION_CONTEXT_PROPERTY_HOST_USER_STATE

The value is a pointer to the host state specified on the <a href="https://msdn.microsoft.com/42e4d24d-5611-4561-b874-6dc3f3f88c73">service host</a> as the 
                    <a href="https://msdn.microsoft.com/305fe7ad-e4a2-499a-b34b-e5b7cde53e22">WS_SERVICE_PROPERTY_HOST_USER_STATE</a> service property. This property is available to 
                     service operations  and to the <a href="https://msdn.microsoft.com/2fcd8905-7002-41b8-b947-14d53c889c21">WS_SERVICE_MESSAGE_RECEIVE_CALLBACK</a>.
                


### -field WS_OPERATION_CONTEXT_PROPERTY_CHANNEL_USER_STATE

The value is a pointer to the channel state specified through <a href="https://msdn.microsoft.com/473af4be-d193-42a5-82ff-359b50a7bc58">WS_SERVICE_ACCEPT_CHANNEL_CALLBACK</a>. This property is 
                    available to  service operations and to the <a href="https://msdn.microsoft.com/2fcd8905-7002-41b8-b947-14d53c889c21">WS_SERVICE_MESSAGE_RECEIVE_CALLBACK</a>.
                


### -field WS_OPERATION_CONTEXT_PROPERTY_INPUT_MESSAGE

The value is a pointer to the underlying input message. This property is available to service operations and to the 
                    <a href="https://msdn.microsoft.com/2fcd8905-7002-41b8-b947-14d53c889c21">WS_SERVICE_MESSAGE_RECEIVE_CALLBACK</a>.
                


### -field WS_OPERATION_CONTEXT_PROPERTY_OUTPUT_MESSAGE

The value is a pointer to the underlying output message. This property is available only to service operations.
                


### -field WS_OPERATION_CONTEXT_PROPERTY_HEAP

The value is a pointer to the WS_HEAP. This property is available to a service operation. Please see the memory management section in 
                    service operations for usage.
                


### -field WS_OPERATION_CONTEXT_PROPERTY_LISTENER


### -field WS_OPERATION_CONTEXT_PROPERTY_ENDPOINT_ADDRESS



