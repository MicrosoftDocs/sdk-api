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

# MI_Context_PostError function


## -description


Providers call this function to post a return code to the client in response to a request.


## -parameters




### -param context [in]

A pointer to the request context.


### -param resultCode

The Result code to be sent to the client.


### -param resultType

A null-terminated string that represents the type of the result code. The string can be one of these values or an arbitrary value defined by the provider.



#### MI_RESULT_TYPE_MI ("MI")

MI result type



#### MI_RESULT_TYPE_HRESULT ("HRESULT")

HRESULT (COM return type) result type



#### MI_RESULT_TYPE_WIN32 ("WIN32")

Win32 result type


### -param errorMessage

A null-terminated string that represents the error message to be sent to the client. The message should be in the requested UI locale, if possible.


## -returns



This function returns MI_INLINE MI_Result MI_INLINE_CALL.




## -remarks



After an error is posted, the request context must not be used, because it becomes invalid at this point.




## -see-also




<a href="https://msdn.microsoft.com/51d6c510-f9fd-4ab7-a669-b2a5776b496d">MI_Context</a>



<a href="https://msdn.microsoft.com/7626b488-58a3-4c9c-a80b-9b0a6dd7f533">MI_Context_WriteError</a>
 

 

