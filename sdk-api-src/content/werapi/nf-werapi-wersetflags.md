---
UID: NF:werapi.WerSetFlags
title: WerSetFlags function (werapi.h)
description: Sets the Windows Error Reporting (WER) reporting settings for the current process.
helpviewer_keywords: ["WER_FAULT_REPORTING_ALWAYS_SHOW_UI","WER_FAULT_REPORTING_FLAG_DISABLE_THREAD_SUSPENSION","WER_FAULT_REPORTING_FLAG_NOHEAP","WER_FAULT_REPORTING_FLAG_QUEUE","WER_FAULT_REPORTING_FLAG_QUEUE_UPLOAD","WerSetFlags","WerSetFlags function [Windows Error Reporting]","base.wersetflags","wer.wersetflags","werapi/WerSetFlags"]
old-location: wer\wersetflags.htm
tech.root: wer
ms.assetid: 2a71203f-3a08-461f-a230-e3fee00d9d99
ms.date: 07/26/2023
ms.keywords: WER_FAULT_REPORTING_ALWAYS_SHOW_UI, WER_FAULT_REPORTING_FLAG_DISABLE_THREAD_SUSPENSION, WER_FAULT_REPORTING_FLAG_NOHEAP, WER_FAULT_REPORTING_FLAG_QUEUE, WER_FAULT_REPORTING_FLAG_QUEUE_UPLOAD, WerSetFlags, WerSetFlags function [Windows Error Reporting], base.wersetflags, wer.wersetflags, werapi/WerSetFlags
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
 - WerSetFlags
 - werapi/WerSetFlags
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
 - WerSetFlags
---

# WerSetFlags function

## -description

Sets the [Windows Error Reporting](../_wer/index.md) (WER) settings for the current process.

## -parameters

### -param dwFlags [in]

The fault reporting settings. You can specify one or more of the following values:

|Value|Meaning|
|--- |--- |
|**WER_FAULT_REPORTING_FLAG_DISABLE_THREAD_SUSPENSION**|Do not suspend the process threads before reporting the error.|
|**WER_FAULT_REPORTING_FLAG_NOHEAP**|Do not collect heap information in the event of an application crash or non-response.|
|**WER_FAULT_REPORTING_FLAG_QUEUE**|Queue critical reports.|
|**WER_FAULT_REPORTING_FLAG_QUEUE_UPLOAD**|Queue critical reports and upload from the queue.|
|**WER_FAULT_REPORTING_ALWAYS_SHOW_UI**|Always show error reporting UI for this process. This is applicable for interactive applications only.|

## -returns

This function returns **S_OK** on success or an error code on failure.

## -see-also

[WerGetFlags](/windows/desktop/api/werapi/nf-werapi-wergetflags), [Windows Error Reporting](/windows/desktop/wer)
