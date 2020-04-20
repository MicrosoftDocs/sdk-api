---
UID: NS:werapi._WER_RUNTIME_EXCEPTION_INFORMATION
title: WER_RUNTIME_EXCEPTION_INFORMATION (werapi.h)
description: Contains the exception information that you use to determine whether you want to claim the crash.helpviewer_keywords: ["*PWER_RUNTIME_EXCEPTION_INFORMATION","PWER_RUNTIME_EXCEPTION_INFORMATION","PWER_RUNTIME_EXCEPTION_INFORMATION structure pointer [Windows Error Reporting]","WER_RUNTIME_EXCEPTION_INFORMATION","WER_RUNTIME_EXCEPTION_INFORMATION structure [Windows Error Reporting]","wer.wer_runtime_exception_information","werapi/PWER_RUNTIME_EXCEPTION_INFORMATION","werapi/WER_RUNTIME_EXCEPTION_INFORMATION"]
old-location: wer\wer_runtime_exception_information.htm
tech.root: wer
ms.assetid: fcf956ac-6015-439c-aec6-8f6a826ff269
ms.date: 12/05/2018
ms.keywords: '*PWER_RUNTIME_EXCEPTION_INFORMATION, PWER_RUNTIME_EXCEPTION_INFORMATION, PWER_RUNTIME_EXCEPTION_INFORMATION structure pointer [Windows Error Reporting], WER_RUNTIME_EXCEPTION_INFORMATION, WER_RUNTIME_EXCEPTION_INFORMATION structure [Windows Error Reporting], wer.wer_runtime_exception_information, werapi/PWER_RUNTIME_EXCEPTION_INFORMATION, werapi/WER_RUNTIME_EXCEPTION_INFORMATION'
f1_keywords:
- werapi/WER_RUNTIME_EXCEPTION_INFORMATION
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Werapi.h
api_name:
- WER_RUNTIME_EXCEPTION_INFORMATION
targetos: Windows
req.typenames: WER_RUNTIME_EXCEPTION_INFORMATION, *PWER_RUNTIME_EXCEPTION_INFORMATION
req.redist: 
ms.custom: 19H1
---

# WER_RUNTIME_EXCEPTION_INFORMATION structure


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

An <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-exception_record">EXCEPTION_RECORD</a> structure that contains the exception information.


### -field context

A <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-arm64_nt_context">CONTEXT</a> structure that contains the context information.


### -field pwszReportId

A pointer to a constant, null-terminated string that contains the size of the exception information.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/werapi/nc-werapi-pfn_wer_runtime_exception_event">OutOfProcessExceptionEventCallback</a>
 

 

