---
UID: NF:werapi.WerGetFlags
title: WerGetFlags function (werapi.h)
description: Retrieves the fault reporting settings for the specified process.
helpviewer_keywords: ["WER_FAULT_REPORTING_ALWAYS_SHOW_UI","WER_FAULT_REPORTING_FLAG_DISABLE_THREAD_SUSPENSION","WER_FAULT_REPORTING_FLAG_NOHEAP","WER_FAULT_REPORTING_FLAG_QUEUE","WER_FAULT_REPORTING_FLAG_QUEUE_UPLOAD","WerGetFlags","WerGetFlags function [Windows Error Reporting]","base.wergetflags","wer.wergetflags","werapi/WerGetFlags"]
old-location: wer\wergetflags.htm
tech.root: wer
ms.assetid: 8c5f08c0-e2d1-448c-9a57-ef19897f64c6
ms.date: 07/21/2023
ms.keywords: WER_FAULT_REPORTING_ALWAYS_SHOW_UI, WER_FAULT_REPORTING_FLAG_DISABLE_THREAD_SUSPENSION, WER_FAULT_REPORTING_FLAG_NOHEAP, WER_FAULT_REPORTING_FLAG_QUEUE, WER_FAULT_REPORTING_FLAG_QUEUE_UPLOAD, WerGetFlags, WerGetFlags function [Windows Error Reporting], base.wergetflags, wer.wergetflags, werapi/WerGetFlags
req.header: werapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WerGetFlags
 - werapi/WerGetFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-windowserrorreporting-l1-1-3.dll
 - api-ms-win-core-windowserrorreporting-l1-1-2.dll
 - api-ms-win-core-windowserrorreporting-l1-1-1.dll
 - Kernel32.dll
 - API-MS-Win-Core-Windowserrorreporting-l1-1-0.dll
 - KernelBase.dll
api_name:
 - WerGetFlags
---

# WerGetFlags function

## -description

Retrieves the [Windows Error Reporting](../_wer/index.md) (WER) fault reporting settings for the specified process.

## -parameters

### -param hProcess [in]

A handle to the process. This handle must have the PROCESS_VM_READ or PROCESS_QUERY_INFORMATION access right.

### -param pdwFlags [out]

This parameter can contain one or more of the following values.

|Value|Meaning|
|--- |--- |
|**WER_FAULT_REPORTING_FLAG_DISABLE_THREAD_SUSPENSION**|Do not suspend the process threads before reporting the error.|
|**WER_FAULT_REPORTING_FLAG_NOHEAP**|Do not collect heap information in the event of an application crash or non-response.|
|**WER_FAULT_REPORTING_FLAG_QUEUE**|Queue critical reports for the specified process. This does not show any UI.|
|**WER_FAULT_REPORTING_FLAG_QUEUE_UPLOAD**|Queue critical reports and upload from the queue.|
|**WER_FAULT_REPORTING_ALWAYS_SHOW_UI**|Always show error reporting UI for this process. This is applicable for interactive applications only.|

## -returns

This function returns **S_OK** on success or an error code on failure.

## -see-also

[WerSetFlags](/windows/desktop/api/werapi/nf-werapi-wersetflags), [Windows Error Reporting](/windows/desktop/wer)
