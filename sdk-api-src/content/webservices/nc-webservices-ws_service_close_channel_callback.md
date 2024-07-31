---
UID: NC:webservices.WS_SERVICE_CLOSE_CHANNEL_CALLBACK
title: WS_SERVICE_CLOSE_CHANNEL_CALLBACK (webservices.h)
description: Invoked when a channel is closed or aborted on an endpoint.
helpviewer_keywords: ["WS_SERVICE_CLOSE_CHANNEL_CALLBACK","WS_SERVICE_CLOSE_CHANNEL_CALLBACK callback","WS_SERVICE_CLOSE_CHANNEL_CALLBACK callback function [Web Services for Windows]","webservices/WS_SERVICE_CLOSE_CHANNEL_CALLBACK","wsw.ws_service_close_channel_callback"]
old-location: wsw\ws_service_close_channel_callback.htm
tech.root: wsw
ms.assetid: e2860015-219b-46be-921d-7ced0d95fc60
ms.date: 12/05/2018
ms.keywords: WS_SERVICE_CLOSE_CHANNEL_CALLBACK, WS_SERVICE_CLOSE_CHANNEL_CALLBACK callback, WS_SERVICE_CLOSE_CHANNEL_CALLBACK callback function [Web Services for Windows], webservices/WS_SERVICE_CLOSE_CHANNEL_CALLBACK, wsw.ws_service_close_channel_callback
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
 - WS_SERVICE_CLOSE_CHANNEL_CALLBACK
 - webservices/WS_SERVICE_CLOSE_CHANNEL_CALLBACK
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
 - WS_SERVICE_CLOSE_CHANNEL_CALLBACK
---

# WS_SERVICE_CLOSE_CHANNEL_CALLBACK callback function


## -description

Invoked when a channel is closed or aborted on an endpoint. 
                This callback is called right before we are about to close the channel. 
            

For normal operation when service host is running and the client cleanly 
                closed the channel, this implies that we have received a session closure 
                from the client and we are about to close the channel. 
            

The other scenario is when service host is going through an Abort Shutdown 
                or during the processing of the message an unrecoverable error condition is 
                met, as a result of this we attempt to abort and then close the channel. 
                In this case as well right before the abort we will call upon this callback. 
            

For session-based service contract, this notification 
                signifies session tear down. Thus an application state scoped for the session 
                can be destroyed within this callback.

## -parameters

### -param context [in]

The operation context.

### -param asyncContext [in, optional]

Information on whether the function is getting invoked asynchronously.

## -returns

This callback function does not return a value.

## -remarks

The returned HRESULT is only used to see if the function is completing asynchronously. Failure or 
                reporting failure through HRESULT does not in any way affects the service host infrastructure.
                
            

Irrespective of whether <a href="/windows/desktop/api/webservices/nc-webservices-ws_service_accept_channel_callback">WS_SERVICE_ACCEPT_CHANNEL_CALLBACK</a> competed successfully or not. This function 
                will always be fired.
            

See also <a href="/windows/desktop/api/webservices/nc-webservices-ws_service_accept_channel_callback">WS_SERVICE_ACCEPT_CHANNEL_CALLBACK</a> which can be used by the application to associate state,
                and gets called when a channel gets accepted.
            

For an example implementation on how to use this callback for disassociating session state, see the session based calculator <a href="/windows/desktop/wsw/sessionfullcalculatorserviceexample">sample</a>.
            

This callback is cancellable.
            


#### Examples


``` syntax
HRESULT CALLBACK FreeSessionCalculator (const WS_OPERATION_CONTEXT* context,
                                        const WS_ASYNC_CONTEXT* asyncContext)
{
     HRESULT hr = NOERROR;
     SessionfulCalculator* calculator = NULL;
     hr = WsGetOperationContextProperty (context, 
                                         WS_OPERATION_CONTEXT_PROPERTY_CHANNEL_USER_STATE, 
                                         &calculator, sizeof (SessionfulCalculator*), NULL);
     if (SUCCEEDED(hr) && (calculator != NULL))
     {                                                       
         delete calculator;
     }
     return NOERROR;
}

```

