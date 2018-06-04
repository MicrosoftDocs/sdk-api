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

# MI_Utilities_CimErrorFromErrorCode function


## -description


Maps an operating-system specific error code to a CIM error instance.


## -parameters




### -param error

Error code to translate.


### -param errorType [in]

One of the following error types.



#### MI_RESULT_TYPE_MI

<b>MI</b> result type



#### MI_RESULT_TYPE_HRESULT

<b>HRESULT</b> (COM return type) result type



#### MI_RESULT_TYPE_WIN32

<b>Win32</b> result type


### -param errorMessage [in]

Error message to encode in the CIM error instance.


### -param cimError

Returned CIM error instance. This must be deleted by using the <a href="https://msdn.microsoft.com/6370e464-b262-4c91-a3c8-889911df7965">MI_Instance_Delete</a> function.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.



