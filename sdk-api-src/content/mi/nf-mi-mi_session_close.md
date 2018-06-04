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

# MI_Session_Close function


## -description


Closes a session and releases all associated memory.


## -parameters




### -param session [in, out]

Session handle returned from <a href="https://msdn.microsoft.com/76010766-aa20-4632-940d-48d9769803da">MI_Application_NewSession</a>.


### -param completionContext [in, optional]

Optional parameter to be returned through the <b>completionCallback</b> callback.


### -param completionCallback [in, out]

Optional callback to make the session close asynchronous.  (If this value is <b>NULL</b>, then the close call is synchronous.) If the <b>MI_Session_Close</b> is called from a callback the completion callback must be specified.  Not doing so can result in a deadlock.



#### completionContext


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -remarks



Closing a session will cause all operations that are currently running to be canceled.  Canceling operations will cause asynchronous operation callbacks to be called (with the final result of an MI_Operation_Get* function call's <i>moreResults</i> parameter equal to <b>MI_FALSE</b>, although more than one result may be delivered before this happens).  Not closing all operation handles that were created with the current session will cause the closing of the session to stop responding for synchronous calls and the asynchronous callback will not be called.  Operation and session handles not fully closed will cause the application handle to stop responding during shutdown.



