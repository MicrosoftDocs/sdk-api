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

# WS_ASYNC_FUNCTION callback function


## -description



                Used with the <a href="https://msdn.microsoft.com/8705ac1a-62ba-4239-aeb6-b35ac5f0dd18">WsAsyncExecute</a> to specify the next 
                function to invoke in a series of async operations.
            


## -parameters




### -param hr [in]


                The result of the previous async operation.
                


### -param callbackModel [in]


                    Whether the callback is being invoked long or short.
                    For more information, see <a href="https://msdn.microsoft.com/6a8e4c0b-3c0a-4bd3-bbac-40e6f499a055">WS_CALLBACK_MODEL</a>.
                


### -param *callbackState [in]


                    This user supplied value that was passed to <a href="https://msdn.microsoft.com/8705ac1a-62ba-4239-aeb6-b35ac5f0dd18">WsAsyncExecute</a>/
                


### -param *next


                    Set the function field to the next function to call.  It will be called regardless of whether or not the current function succeeds or fails.
                


                    Set the function field to <b>NULL</b> to indicate that there are no more functions to call.  
                


<a href="https://msdn.microsoft.com/8705ac1a-62ba-4239-aeb6-b35ac5f0dd18">WsAsyncExecute</a> will set the function field to <b>NULL</b> before each function is called.
                


### -param *asyncContext [in, optional]

Information on how to invoke the function asynchronously, or <b>NULL</b> if invoking synchronously.


### -param *error [in, optional]


                    Specifies where additional error information should be stored if the function fails.
                


## -returns



This callback function does not return a value.



