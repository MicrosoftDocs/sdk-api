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



