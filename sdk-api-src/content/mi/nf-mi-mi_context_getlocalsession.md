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

# MI_Context_GetLocalSession function


## -description


Gets the local session (<a href="https://msdn.microsoft.com/68a69321-0aa9-423e-a72f-aa2f4dee2d51">MI_Session</a>) which allows the provider to perform CIM operations against  the local server hosting the provider.


## -parameters




### -param context [in]

A pointer to the request context.


### -param session [out]

A pointer to the returned <a href="https://msdn.microsoft.com/68a69321-0aa9-423e-a72f-aa2f4dee2d51">MI_Session</a> object. This session must not be closed.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -remarks



This session is pre-instantiated and has the lifetime of the context from which the session was obtained. The provider must not close this session because its lifetime is bound to the context.

The provider should call this function rather than creating a new session through the <a href="https://msdn.microsoft.com/76010766-aa20-4632-940d-48d9769803da">MI_Application_NewSession</a> function, because some optimizations may be possible for talking to the CIM server.

The security context used to call the <b>MI_Context_GetLocalSession</b> function should be the same identity used communicate back to the server through the MI_Session_* operation functions. Do not cache these sessions outside the current operation. The provider calls this method multiple times within an operation under different identities, in which case the retrieved session should also be used with the same identity. Any operations on the session should always be the same identity that the user retrieved for the local session, or else the operation could fail with the <b>MI_RESULT_ACCESS_DENIED</b> return code.



