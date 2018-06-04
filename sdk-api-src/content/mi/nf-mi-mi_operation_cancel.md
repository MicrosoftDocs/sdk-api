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

# MI_Operation_Cancel function


## -description


Cancels a running operation.


## -parameters




### -param operation [in, out]

A pointer to an operation handle that was returned from a call to one of the <a href="https://msdn.microsoft.com/68a69321-0aa9-423e-a72f-aa2f4dee2d51">MI_Session</a> operation functions.  For asynchronous callbacks, this value can be the operation handle that is passed into the callback.


### -param reason


<a href="https://msdn.microsoft.com/3c498055-03ef-4163-9de5-cf4e70051cea">MI_CancellationReason</a> enumeration value.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -remarks



Cancellation is asynchronous.  Cancelled operations still need to be closed.  Cancellation will cause the operation to finish as soon as possible. For an asynchronous operation, this will cause final callback to happen with the final result. For a synchronous operation, the final result should be available soon.

A closing operation, such as <b>MI_Operations_Cancel</b>, should be called in same security context as the starting operation.

After cancellation, there may be more than just one result, because cancellation happens as soon as possible, so a few extra results may still get delivered.  Not all operation cancellations get through to the provider for notification, though. (For example, enum can, but invoke cannot.)  The client does disconnect from the server as soon as possible, though, so it will not wait for the entire operation to complete before giving a final result.  Because not all operation cancellation can get to the server, it means that if the operation is taking quota (in terms of running operations, memory usage, and so on), then new operations may possibly fail with quota violations until the provider finally realizes the operation is canceled, and it shuts itself down.



