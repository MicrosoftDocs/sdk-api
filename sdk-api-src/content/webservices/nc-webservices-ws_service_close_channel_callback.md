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




### -param *context [in]


                    The operation context.
                


### -param *asyncContext [in, optional]

Information on whether the function is getting invoked asynchornously.


## -returns



This callback function does not return a value.




## -remarks




                The returned HRESULT is only used to see if the function is completing asynchronously. Failure or 
                reporting failure through HRESULT does not in any way affects the service host infrastructure.
                
            


                Irrespective of whether <a href="https://msdn.microsoft.com/473af4be-d193-42a5-82ff-359b50a7bc58">WS_SERVICE_ACCEPT_CHANNEL_CALLBACK</a> competed successfully or not. This function 
                will always be fired.
            


                See also <a href="https://msdn.microsoft.com/473af4be-d193-42a5-82ff-359b50a7bc58">WS_SERVICE_ACCEPT_CHANNEL_CALLBACK</a> which can be used by the application to associate state,
                and gets called when a channel gets accepted.
            


                For an example implementation on how to use this callback for disassociating session state, see the session based calculator <a href="https://msdn.microsoft.com/7501025b-5692-4f89-ad74-c60694c29163">sample</a>.
            


                This callback is cancellable.
            


#### Examples

<pre class="syntax" xml:space="preserve"><code>HRESULT CALLBACK FreeSessionCalculator (const WS_OPERATION_CONTEXT* context,
                                        const WS_ASYNC_CONTEXT* asyncContext)
{
     HRESULT hr = NOERROR;
     SessionfulCalculator* calculator = NULL;
     hr = WsGetOperationContextProperty (context, 
                                         WS_OPERATION_CONTEXT_PROPERTY_CHANNEL_USER_STATE, 
                                         &amp;calculator, sizeof (SessionfulCalculator*), NULL);
     if (SUCCEEDED(hr) &amp;&amp; (calculator != NULL))
     {                                                       
         delete calculator;
     }
     return NOERROR;
}
</code></pre>


