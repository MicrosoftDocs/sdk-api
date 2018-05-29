---
UID: NF:webservices.WsAsyncExecute
title: WsAsyncExecute function
author: windows-sdk-content
description: Helper function for implementing an asynchronous operation.
old-location: wsw\wsasyncexecute.htm
old-project: wsw
ms.assetid: 8705ac1a-62ba-4239-aeb6-b35ac5f0dd18
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: WsAsyncExecute, WsAsyncExecute function [Web Services for Windows], webservices/WsAsyncExecute, wsw.wsasyncexecute
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WS_SECURITY_ALGORITHM_PROPERTY_ID
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	WebServices.dll
api_name:
-	WsAsyncExecute
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsAsyncExecute function


## -description



Helper function for implementing an <a href="https://msdn.microsoft.com/d0b3f154-2219-4085-a652-e9aeb126598c">asynchronous</a> operation.




## -parameters




### -param asyncState [in]


                    A pointer to the <a href="https://msdn.microsoft.com/ca7f14a9-bee8-46ed-a082-7e64a41f7493">WS_ASYNC_STATE</a> structure used during the asynchronous operation.  This is a state maintenance parameter not intended
                for direct use.  The application must allocate  the <b>WS_ASYNC_STATE</b> structure and ensure that it 
                is kept alive during the entire asynchronous operation.  The <b>WS_ASYNC_STATE</b> structure can be reused after an 
                asynchronous operation has completed.
            


### -param operation [in, optional]

Represents the initial asynchronous operation to be performed.
                


### -param callbackModel [in]


                    Indicates whether the callback is being invoked long or short.
                For more information, see <a href="https://msdn.microsoft.com/6a8e4c0b-3c0a-4bd3-bbac-40e6f499a055">WS_CALLBACK_MODEL</a>



### -param callbackState [in]


                    A void pointer to a user-defined value that is passed to each <a href="https://msdn.microsoft.com/5645424b-4ca4-4f5d-b58d-16f3a7cceb6b">WS_ASYNC_FUNCTION</a>.
                


### -param asyncContext [in, optional]

Pointer to information for invoking the function asynchronously. Pass <b>NULL</b> to invoke the function synchronously.


### -param error [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> structure  that receives additional error information if the function fails.
                


## -returns



If the function succeeds, it returns NO_ERROR; otherwise, it returns an HRESULT error code.




## -remarks



For an understaning of how WWSAPI handles asynchronous operations, see the <a href="https://msdn.microsoft.com/d0b3f154-2219-4085-a652-e9aeb126598c">Asynchronous Model</a> topic. 

In many cases, an asynchronous operation is composed of other asynchronous operations. Each asynchronous operation may return WS_S_ASYNC indicating the callback will be invoked, or any other success or failure code, in which case the callback will not be invoked. The operation must be prepared to accept a <b>NULL</b> WS_ASYNC_CONTEXT indicating that the caller is requesting the operation to be performed synchronously. It must also ensure that the callback is invoked appropriately. In complex asynchronous operations,  <b>WsAsyncExecute</b> simplifies these details.

<b>WsAsyncExecute</b> operates by invoking a user-defined callback which can initiate an asynchrnous operation and indicate a function to be invoked when the asynchronous operation is complete. This sequence continues until the callback does not set another function to invoke. At this point, the callback specified by the WS_ASYNC_CONTEXT will be invoked if any of the operations completed asynchronously. 



The <a href="https://msdn.microsoft.com/ca7f14a9-bee8-46ed-a082-7e64a41f7493">WS_ASYNC_STATE</a> parameter is used by <b>WsAsyncExecute</b> to maintain its state, and is not intended to be initialized, inspected, or used by the caller. The caller however, must allocate the <b>WS_ASYNC_STATE</b> and ensure that it is kept alive during the entire asynchronous operation. The <b>WS_ASYNC_STATE</b> may be reused once the asynchronous operation is complete.


                The examples <a href="https://msdn.microsoft.com/e60a4005-4849-4603-ae25-b88da8628f80">AsyncAdd3ExplicitExample</a> and <a href="https://msdn.microsoft.com/f84de03f-ecfb-494e-9a1d-a96d399a41c0">AsyncAdd3ImplicitExample</a> demonstrate implementing
                the same asynchronous function manually using <b>WsAsyncExecute</b>.
            



