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

# MI_Operation_Close function


## -description


Closes an operation handle.


## -parameters




### -param operation [in, out]

A pointer to an operation handle that was returned from a call to one of the 
      <a href="https://msdn.microsoft.com/68a69321-0aa9-423e-a72f-aa2f4dee2d51">MI_Session</a> operation functions. For asynchronous 
      callbacks, it can also be the operation handle that is passed into the callback.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the 
      function return code. This can be one of the following codes.




## -remarks



For synchronous operations, the close function is synchronous on retrieving the final result, so if the client 
     does not retrieve all results, then this call will fail. For asynchronous operations, this function will not 
     block.

A closing operation, such as <b>MI_Operations_Close</b>, should be called in same security 
     context as the starting operation.



