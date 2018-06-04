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

# MI_Context_SetStringOption function


## -description


Sets a context-specific option.


## -parameters




### -param context [in]

Request context.


### -param name

A null-terminated string that represents the name of the option to change.


### -param value

A null-terminated string that represents the new value for the specified option.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -remarks



This function allows the provider to adjust the server's behavior.

On Windows Server 2012, this function only supports the "SECURITY" option, which is used only by an indication provider to control which users have permission to subscribe to the indication class. The function is valid if and only if it is called inside the indication class's *_Load function.




## -see-also




<a href="https://msdn.microsoft.com/51d6c510-f9fd-4ab7-a669-b2a5776b496d">MI_Context</a>



<a href="https://msdn.microsoft.com/3338ca5c-48ac-450f-bf2a-ded6a2c3da19">MI_Context_GetCustomOption</a>



<a href="https://msdn.microsoft.com/f4f6c935-5207-46f6-b015-c4db724113f3">MI_Context_GetCustomOptionAt</a>



<a href="https://msdn.microsoft.com/8cce1492-5c3a-4ba8-8f33-22f6ff7fcf3a">MI_Context_GetCustomOptionCount</a>



<a href="https://msdn.microsoft.com/862a44b9-a6bd-4433-a7da-9309392a946c">MI_Context_GetNumberOption</a>



<a href="https://msdn.microsoft.com/ef6fa103-7421-4c66-902d-c5a731abaa54">MI_Context_GetStringOption</a>
 

 

