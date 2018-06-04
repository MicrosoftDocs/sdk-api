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

# WS_SERVICE_ACCEPT_CHANNEL_CALLBACK callback function


## -description


Invoked when a channel is accepted on an endpoint 
                listener by service host.
            


                For session-based service contract, this notification signifies session initiation. 
                Thus an application state scoped for the session can be created within this callback. 
            


## -parameters




### -param *context [in]


                    The operation context.
                


#### - **channelState


                    The callback may provide channel state through this parameter. This channel state is
                    made available to the service operation as part of <a href="https://msdn.microsoft.com/5c9b5906-15f0-4339-a4ad-39977d28ce5b">WS_OPERATION_CONTEXT</a> through
                    the <a href="https://msdn.microsoft.com/71f7d0fe-c120-4667-93de-a0dfb94fccc1">WS_OPERATION_CONTEXT_PROPERTY_CHANNEL_USER_STATE</a>.
                


### -param *asyncContext [in, optional]

Information on whether the function is getting invoked asynchornously.


### -param *error [in, optional]


                    Specifies where additional error information should be stored if the function fails.
                


#### - channelState


                    The callback may provide channel state through this parameter. This channel state is
                    made available to the service operation as part of <a href="https://msdn.microsoft.com/5c9b5906-15f0-4339-a4ad-39977d28ce5b">WS_OPERATION_CONTEXT</a> through
                    the <a href="https://msdn.microsoft.com/71f7d0fe-c120-4667-93de-a0dfb94fccc1">WS_OPERATION_CONTEXT_PROPERTY_CHANNEL_USER_STATE</a>.
                


## -returns



This callback function does not return a value.




## -remarks




                See also <a href="https://msdn.microsoft.com/e2860015-219b-46be-921d-7ced0d95fc60">WS_SERVICE_CLOSE_CHANNEL_CALLBACK</a> which can be used by the application to disassociate state,
                and gets called on channel closure.
            


                This callback is cancellable.
            


#### Examples


                For an example implementation on how to use this callback for associating session state, see the session based calculator <a href="https://msdn.microsoft.com/7501025b-5692-4f89-ad74-c60694c29163">sample</a>.
            

<div class="code"></div>
<pre class="syntax" xml:space="preserve"><code>HRESULT CALLBACK CreateSessionCalculator (const WS_OPERATION_CONTEXT* context, void** userChannelState,
                                          const WS_ASYNC_CONTEXT* asyncContext, WS_ERROR* error)
{
    SessionfullCalculator* calculator = new SessionfullCalculator ();
    if (calculator != NULL)
        *userChannelState = (void*) calculator;
    else
        return E_OUTOFMEMORY;
    return NOERROR;
}</code></pre>


