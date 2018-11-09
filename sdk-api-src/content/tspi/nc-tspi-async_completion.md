---
UID: NC:tspi.ASYNC_COMPLETION
title: ASYNC_COMPLETION
author: windows-sdk-content
description: Completion_Proc is a callback function implemented by TAPI and supplied to the service provider as a parameter to TSPI_providerInit.
old-location: tspi\completion_proc.htm
tech.root: tapi
ms.assetid: 673c9d23-e380-49f7-bd06-23552634d5b9
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: ASYNC_COMPLETION, ASYNC_COMPLETION callback, CompletionProc, CompletionProc callback function [TAPI 2.2], _tspi_async_completion, tspi.async_completion, tspi.completion_proc, tspi/CompletionProc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: tspi.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Tspi.h
api_name:
 - CompletionProc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ASYNC_COMPLETION callback function


## -description


<i>Completion_Proc</i> is a callback function implemented by TAPI and supplied to the service provider as a parameter to 
<a href="https://msdn.microsoft.com/6cb7817b-6df3-4a6a-a666-b41c2eb0b118">TSPI_providerInit</a>. The service provider calls this function to report the completion of a line or phone procedure that it executes asynchronously.

The <b>ASYNC_COMPLETION</b> type defines a pointer to this callback function. <i>Completion_Proc</i> is a placeholder for the application-defined function name.


## -parameters




### -param dwRequestID

The identifier passed in the original request that the service provider executed asynchronously.


### -param lResult

The outcome of the operation. This can be zero to indicate success or a negative number to indicate an error. The possible specific error values that can result from a function are the same for asynchronous or synchronous execution.


## -returns



This function has no return value.




## -remarks



The call state when calling this function can be any state.

This procedure is supplied by TAPI at the time a service provider is initialized with the 
<a href="https://msdn.microsoft.com/6cb7817b-6df3-4a6a-a666-b41c2eb0b118">TSPI_providerInit</a> function. Some of the TSPI procedures that operate on line, call, and phone devices specify asynchronous operation. These procedures include a <i>dwRequestID</i> parameter to identify the request. When such a procedure is called, the service provider can return a negative number for an error if one is detected immediately, or the positive <i>dwRequestID</i> if the operation continues asynchronously. The service provider must report completion exactly once for each request it executes asynchronously. It does so by calling this procedure. The service provider is not permitted to call this procedure or the 
<a href="https://msdn.microsoft.com/11ae7e78-8a10-4757-886b-c0aa47c4d55b">Line_Event</a> or 
<a href="https://msdn.microsoft.com/0b5745a4-7652-48ce-9e8a-eef52c09455f">Phone_Event</a> procedure again until this procedure returns.

The service provider is permitted to call the 
<i>Completion_Proc</i> function before it returns from the first request. TAPI guarantees not to call the service provider from within the 
<i>Completion_Proc</i> context except where noted.

This does not have any direct correspondence at the TAPI level because at that level asynchronous function completions are reported as a message passed through the same callback interface that is used for spontaneous event messages. At the TSPI level, spontaneous events are reported through the 
<a href="https://msdn.microsoft.com/11ae7e78-8a10-4757-886b-c0aa47c4d55b">Line_Event</a> and 
<a href="https://msdn.microsoft.com/0b5745a4-7652-48ce-9e8a-eef52c09455f">Phone_Event</a> callback procedures.




## -see-also




<a href="https://msdn.microsoft.com/11ae7e78-8a10-4757-886b-c0aa47c4d55b">Line_Event</a>



<a href="https://msdn.microsoft.com/0b5745a4-7652-48ce-9e8a-eef52c09455f">Phone_Event</a>



<a href="https://msdn.microsoft.com/6cb7817b-6df3-4a6a-a666-b41c2eb0b118">TSPI_providerInit</a>
 

 

