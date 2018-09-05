---
UID: NC:webservices.WS_SERVICE_MESSAGE_RECEIVE_CALLBACK
title: WS_SERVICE_MESSAGE_RECEIVE_CALLBACK
author: windows-sdk-content
description: Invoked when a WS_MESSAGE is received on an endpoint configured with a WS_SERVICE_CONTRACT which has defaultMessageHandlerCallback set.
old-location: wsw\ws_service_message_receive_callback.htm
old-project: wsw
ms.assetid: 2fcd8905-7002-41b8-b947-14d53c889c21
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WS_SERVICE_MESSAGE_RECEIVE_CALLBACK, WS_SERVICE_MESSAGE_RECEIVE_CALLBACK callback, WS_SERVICE_MESSAGE_RECEIVE_CALLBACK callback function [Web Services for Windows], webservices/WS_SERVICE_MESSAGE_RECEIVE_CALLBACK, wsw.ws_service_message_receive_callback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: webservices.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WDSTRANSPORT_TFTP_CAPABILITY, *PWDSTRANSPORT_TFTP_CAPABILITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - WebServices.h
api_name:
 - WS_SERVICE_MESSAGE_RECEIVE_CALLBACK
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WS_SERVICE_MESSAGE_RECEIVE_CALLBACK callback function


## -description


Invoked when a <a href="https://msdn.microsoft.com/22cc39a9-a3a7-4b4d-bdee-0ccac5dc03ee">WS_MESSAGE</a> is received on an endpoint configured 
                with a <a href="https://msdn.microsoft.com/77bd8c1e-0596-44d7-be99-356d052ee6c1">WS_SERVICE_CONTRACT</a> which has defaultMessageHandlerCallback set.

The incoming <a href="https://msdn.microsoft.com/22cc39a9-a3a7-4b4d-bdee-0ccac5dc03ee">WS_MESSAGE</a>, the serviceProxy along with other parameters 
                is made available to the callback through <a href="https://msdn.microsoft.com/5c9b5906-15f0-4339-a4ad-39977d28ce5b">WS_OPERATION_CONTEXT</a>. 
            


## -parameters




### -param *context [in]

The <a href="https://msdn.microsoft.com/5c9b5906-15f0-4339-a4ad-39977d28ce5b">context</a> within which this callback is being invoked. 
                


### -param *asyncContext [in, optional]

Specifies whether the callback can run asynchronously. 
                


### -param *error [in, optional]

Specifies where additional error information should be stored if the function fails.
                


## -returns



This callback function does not return a value.




## -remarks



When defined, callback would disallow all concurrency on a session based channel. If concurrency on a session based channel 
                    is desirable an application should not define <i>WS_SERVICE_MESSAGE_RECEIVE_CALLBACK</i> on the <a href="https://msdn.microsoft.com/77bd8c1e-0596-44d7-be99-356d052ee6c1">WS_SERVICE_CONTRACT</a>.
                

At the time of the invocation of the callback, service model has performed <a href="https://msdn.microsoft.com/e4f92e99-f272-47b5-8eaa-56713b22df7e">WsReadMessageStart</a> on the receiving 
                    <a href="https://msdn.microsoft.com/22cc39a9-a3a7-4b4d-bdee-0ccac5dc03ee">WS_MESSAGE</a>. It is the responsibility of the application implementing <i>WS_SERVICE_MESSAGE_RECEIVE_CALLBACK</i>to process the body and perform <a href="https://msdn.microsoft.com/3112be44-f610-421f-a4ea-0f87fc383540">WsReadMessageEnd</a> operation.
                

 
                    If the callback fails, the underlying channel is aborted.
                

See also,
                    <a href="https://msdn.microsoft.com/4235554e-19a8-4df7-97a5-2f7544a3c830">UnTypedServiceExample</a>



#### Examples

Defining a WS_SERVICE_MESSAGE_RECEIVE_CALLBACK

<pre class="syntax" xml:space="preserve"><code>
// Method contract for the service
static WS_SERVICE_CONTRACT calculatorContract = 
{
    NULL, 
    NULL, 
    DefaultMessageHandlerCallback, // WS_SERVICE_MESSAGE_RECEIVE_CALLBACK
    NULL
};</code></pre>
Accessing the incoming <a href="https://msdn.microsoft.com/22cc39a9-a3a7-4b4d-bdee-0ccac5dc03ee">WS_MESSAGE</a> property
            

<pre class="syntax" xml:space="preserve"><code>HRESULT CALLBACK MessageRecieved(const WS_OPERATION_CONTEXT* context, const WS_ASYNC_CONTEXT* asyncContext, WS_ERROR* error)
{
    :
    hr = WsGetOperationContextProperty(context, WS_OPERATION_CONTEXT_PROPERTY_INPUT_MESSAGE, &amp;requestMessage, sizeof(requestMessage), NULL, error);
    :
}</code></pre>


