---
UID: NC:webservices.WS_SERVICE_MESSAGE_RECEIVE_CALLBACK
title: WS_SERVICE_MESSAGE_RECEIVE_CALLBACK (webservices.h)
description: Invoked when a WS_MESSAGE is received on an endpoint configured with a WS_SERVICE_CONTRACT which has defaultMessageHandlerCallback set.
helpviewer_keywords: ["WS_SERVICE_MESSAGE_RECEIVE_CALLBACK","WS_SERVICE_MESSAGE_RECEIVE_CALLBACK callback","WS_SERVICE_MESSAGE_RECEIVE_CALLBACK callback function [Web Services for Windows]","webservices/WS_SERVICE_MESSAGE_RECEIVE_CALLBACK","wsw.ws_service_message_receive_callback"]
old-location: wsw\ws_service_message_receive_callback.htm
tech.root: wsw
ms.assetid: 2fcd8905-7002-41b8-b947-14d53c889c21
ms.date: 12/05/2018
ms.keywords: WS_SERVICE_MESSAGE_RECEIVE_CALLBACK, WS_SERVICE_MESSAGE_RECEIVE_CALLBACK callback, WS_SERVICE_MESSAGE_RECEIVE_CALLBACK callback function [Web Services for Windows], webservices/WS_SERVICE_MESSAGE_RECEIVE_CALLBACK, wsw.ws_service_message_receive_callback
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_SERVICE_MESSAGE_RECEIVE_CALLBACK
 - webservices/WS_SERVICE_MESSAGE_RECEIVE_CALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - WebServices.h
api_name:
 - WS_SERVICE_MESSAGE_RECEIVE_CALLBACK
---

# WS_SERVICE_MESSAGE_RECEIVE_CALLBACK callback function


## -description

Invoked when a <a href="/windows/desktop/wsw/ws-message">WS_MESSAGE</a> is received on an endpoint configured with a <a href="/windows/desktop/api/webservices/ns-webservices-ws_service_contract">WS_SERVICE_CONTRACT</a> which has defaultMessageHandlerCallback set.

The incoming <a href="/windows/desktop/wsw/ws-message">WS_MESSAGE</a>, the serviceProxy along with other parameters is made available to the callback through <a href="/windows/desktop/wsw/ws-operation-context">WS_OPERATION_CONTEXT</a>.

## -parameters

### -param context [in]

The <a href="/windows/desktop/wsw/ws-operation-context">context</a> within which this callback is being invoked.

### -param asyncContext [in, optional]

Specifies whether the callback can run asynchronously.

### -param error [in, optional]

Specifies where additional error information should be stored if the function fails.

## -returns

This callback function does not return a value.

## -remarks

When defined, callback would disallow all concurrency on a session based channel. If concurrency on a session based channel is desirable an application should not define <i>WS_SERVICE_MESSAGE_RECEIVE_CALLBACK</i> on the <a href="/windows/desktop/api/webservices/ns-webservices-ws_service_contract">WS_SERVICE_CONTRACT</a>.
                

At the time of the invocation of the callback, service model has performed <a href="/windows/desktop/api/webservices/nf-webservices-wsreadmessagestart">WsReadMessageStart</a> on the receiving <a href="/windows/desktop/wsw/ws-message">WS_MESSAGE</a>. It is the responsibility of the application implementing <i>WS_SERVICE_MESSAGE_RECEIVE_CALLBACK</i> to process the body and perform <a href="/windows/desktop/api/webservices/nf-webservices-wsreadmessageend">WsReadMessageEnd</a> operation.
 
If the callback fails, the underlying channel is aborted.
                
See also, <a href="/windows/desktop/wsw/untypedserviceexample">UnTypedServiceExample</a>



#### Examples

Defining a WS_SERVICE_MESSAGE_RECEIVE_CALLBACK


``` syntax

// Method contract for the service
static WS_SERVICE_CONTRACT calculatorContract = 
{
    NULL, 
    NULL, 
    DefaultMessageHandlerCallback, // WS_SERVICE_MESSAGE_RECEIVE_CALLBACK
    NULL
};
```

Accessing the incoming <a href="/windows/desktop/wsw/ws-message">WS_MESSAGE</a> property
            


``` syntax
HRESULT CALLBACK MessageRecieved(const WS_OPERATION_CONTEXT* context, const WS_ASYNC_CONTEXT* asyncContext, WS_ERROR* error)
{
    :
    hr = WsGetOperationContextProperty(context, WS_OPERATION_CONTEXT_PROPERTY_INPUT_MESSAGE, &requestMessage, sizeof(requestMessage), NULL, error);
    :
}
```

