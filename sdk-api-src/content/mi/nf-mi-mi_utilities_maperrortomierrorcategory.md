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

# MI_Utilities_MapErrorToMiErrorCategory function


## -description


Maps an operating system specific error code to an error category.


## -parameters




### -param errorType

A null-terminated string representing an error type. Use one of these constants.



#### MI_RESULT_TYPE_MI

MI result type



#### MI_RESULT_TYPE_HRESULT

HRESULT (COM return type) result type



#### MI_RESULT_TYPE_WIN32

Win32 result type


### -param error

Error code to map.


## -returns



An <a href="https://msdn.microsoft.com/afcc85a1-5aaf-41df-8cd7-b88739b73cf9">MI_ErrorCategory</a> structure that indicates the category of error.




## -see-also




<a href="https://msdn.microsoft.com/afcc85a1-5aaf-41df-8cd7-b88739b73cf9">MI_ErrorCategory</a>
 

 

