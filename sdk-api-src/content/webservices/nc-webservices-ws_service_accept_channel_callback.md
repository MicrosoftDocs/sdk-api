---
UID: NC:webservices.WS_SERVICE_ACCEPT_CHANNEL_CALLBACK
title: WS_SERVICE_ACCEPT_CHANNEL_CALLBACK (webservices.h)
description: Invoked when a channel is accepted on an endpoint listener by service host.
helpviewer_keywords: ["WS_SERVICE_ACCEPT_CHANNEL_CALLBACK","WS_SERVICE_ACCEPT_CHANNEL_CALLBACK callback","WS_SERVICE_ACCEPT_CHANNEL_CALLBACK callback function [Web Services for Windows]","webservices/WS_SERVICE_ACCEPT_CHANNEL_CALLBACK","wsw.ws_service_accept_channel_callback"]
old-location: wsw\ws_service_accept_channel_callback.htm
tech.root: wsw
ms.assetid: 473af4be-d193-42a5-82ff-359b50a7bc58
ms.date: 12/05/2018
ms.keywords: WS_SERVICE_ACCEPT_CHANNEL_CALLBACK, WS_SERVICE_ACCEPT_CHANNEL_CALLBACK callback, WS_SERVICE_ACCEPT_CHANNEL_CALLBACK callback function [Web Services for Windows], webservices/WS_SERVICE_ACCEPT_CHANNEL_CALLBACK, wsw.ws_service_accept_channel_callback
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_SERVICE_ACCEPT_CHANNEL_CALLBACK
 - webservices/WS_SERVICE_ACCEPT_CHANNEL_CALLBACK
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
 - WS_SERVICE_ACCEPT_CHANNEL_CALLBACK
---

# WS_SERVICE_ACCEPT_CHANNEL_CALLBACK callback function


## -description

Invoked when a channel is accepted on an endpoint 
                listener by service host.
            

For session-based service contract, this notification signifies session initiation. 
                Thus an application state scoped for the session can be created within this callback.

## -parameters

### -param context [in]

The operation context.
                


#### - **channelState

The callback may provide channel state through this parameter. This channel state is
                    made available to the service operation as part of <a href="/windows/desktop/wsw/ws-operation-context">WS_OPERATION_CONTEXT</a> through
                    the <a href="/windows/desktop/api/webservices/ne-webservices-ws_operation_context_property_id">WS_OPERATION_CONTEXT_PROPERTY_CHANNEL_USER_STATE</a>.

### -param asyncContext [in, optional]

Information on whether the function is getting invoked asynchronously.

### -param error [in, optional]

Specifies where additional error information should be stored if the function fails.

### -param channelState

The callback may provide channel state through this parameter. This channel state is
                    made available to the service operation as part of <a href="/windows/desktop/wsw/ws-operation-context">WS_OPERATION_CONTEXT</a> through
                    the <a href="/windows/desktop/api/webservices/ne-webservices-ws_operation_context_property_id">WS_OPERATION_CONTEXT_PROPERTY_CHANNEL_USER_STATE</a>.

## -returns

This callback function does not return a value.

## -remarks

See also <a href="/windows/desktop/api/webservices/nc-webservices-ws_service_close_channel_callback">WS_SERVICE_CLOSE_CHANNEL_CALLBACK</a> which can be used by the application to disassociate state,
                and gets called on channel closure.
            

This callback is cancellable.
            


#### Examples

For an example implementation on how to use this callback for associating session state, see the session based calculator <a href="/windows/desktop/wsw/sessionfullcalculatorserviceexample">sample</a>.
            

<div class="code"></div>

``` syntax
HRESULT CALLBACK CreateSessionCalculator (const WS_OPERATION_CONTEXT* context, void** userChannelState,
                                          const WS_ASYNC_CONTEXT* asyncContext, WS_ERROR* error)
{
    SessionfullCalculator* calculator = new SessionfullCalculator ();
    if (calculator != NULL)
        *userChannelState = (void*) calculator;
    else
        return E_OUTOFMEMORY;
    return NOERROR;
}
```

