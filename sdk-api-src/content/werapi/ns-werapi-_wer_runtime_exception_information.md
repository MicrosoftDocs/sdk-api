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

# _WER_RUNTIME_EXCEPTION_INFORMATION structure


## -description


Contains the exception information that you use to determine whether you want to claim the crash.


## -struct-fields




### -field dwSize

Size, in bytes, of this structure.


### -field hProcess

The handle to the process that crashed.


### -field hThread

The handle to the thread that crashed.


### -field exceptionRecord

An <a href="https://msdn.microsoft.com/85a64178-bdcb-4293-9363-289c654730a2">EXCEPTION_RECORD</a> structure that contains the exception information.


### -field context

A <a href="https://msdn.microsoft.com/library/windows/hardware/hh439393">CONTEXT</a> structure that contains the context information.


### -field pwszReportId

A pointer to a constant, null-terminated string that contains the size of the exception information.


## -see-also




<a href="https://msdn.microsoft.com/22033278-2be3-4621-b618-3ccd21fb4cdd">OutOfProcessExceptionEventCallback</a>
 

 

