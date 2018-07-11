---
UID: NS:werapi._WER_RUNTIME_EXCEPTION_INFORMATION
title: "_WER_RUNTIME_EXCEPTION_INFORMATION"
author: windows-sdk-content
description: Contains the exception information that you use to determine whether you want to claim the crash.
old-location: wer\wer_runtime_exception_information.htm
old-project: wer
ms.assetid: fcf956ac-6015-439c-aec6-8f6a826ff269
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: "*PWER_RUNTIME_EXCEPTION_INFORMATION, PWER_RUNTIME_EXCEPTION_INFORMATION, PWER_RUNTIME_EXCEPTION_INFORMATION structure pointer [Windows Error Reporting], WER_RUNTIME_EXCEPTION_INFORMATION, WER_RUNTIME_EXCEPTION_INFORMATION structure [Windows Error Reporting], _WER_RUNTIME_EXCEPTION_INFORMATION, wer.wer_runtime_exception_information, werapi/PWER_RUNTIME_EXCEPTION_INFORMATION, werapi/WER_RUNTIME_EXCEPTION_INFORMATION"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: werapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WER_RUNTIME_EXCEPTION_INFORMATION, *PWER_RUNTIME_EXCEPTION_INFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Werapi.h
api_name:
 - WER_RUNTIME_EXCEPTION_INFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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
 

 

