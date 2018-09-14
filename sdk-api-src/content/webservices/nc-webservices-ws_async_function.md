---
UID: NC:webservices.WS_ASYNC_FUNCTION
title: WS_ASYNC_FUNCTION
author: windows-sdk-content
description: Used with the WsAsyncExecute to specify the next function to invoke in a series of async operations.
old-location: wsw\ws_async_function.htm
tech.root: wsw
ms.assetid: 5645424b-4ca4-4f5d-b58d-16f3a7cceb6b
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: WS_ASYNC_FUNCTION, WS_ASYNC_FUNCTION callback, WS_ASYNC_FUNCTION callback function [Web Services for Windows], webservices/WS_ASYNC_FUNCTION, wsw.ws_async_function
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: v.1.0
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - WebServices.h
api_name:
 - WS_ASYNC_FUNCTION
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



