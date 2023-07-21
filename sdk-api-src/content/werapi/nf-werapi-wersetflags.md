---
UID: NF:werapi.WerSetFlags
title: WerSetFlags function (werapi.h)
description: Sets the fault reporting settings for the current process.
helpviewer_keywords: ["WER_FAULT_REPORTING_ALWAYS_SHOW_UI","WER_FAULT_REPORTING_FLAG_DISABLE_THREAD_SUSPENSION","WER_FAULT_REPORTING_FLAG_NOHEAP","WER_FAULT_REPORTING_FLAG_QUEUE","WER_FAULT_REPORTING_FLAG_QUEUE_UPLOAD","WerSetFlags","WerSetFlags function [Windows Error Reporting]","base.wersetflags","wer.wersetflags","werapi/WerSetFlags"]
old-location: wer\wersetflags.htm
tech.root: wer
ms.assetid: 2a71203f-3a08-461f-a230-e3fee00d9d99
ms.date: 12/05/2018
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
 - Kernel32.dll
 - API-MS-Win-Core-Windowserrorreporting-l1-1-0.dll
 - KernelBase.dll
api_name:
 - WerSetFlags
---

# WerSetFlags function


## -description

Sets the fault reporting settings for the current process.

## -parameters

### -param dwFlags [in]

The fault reporting settings. You can specify one or more of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WER_FAULT_REPORTING_FLAG_DISABLE_THREAD_SUSPENSION"></a><a id="wer_fault_reporting_flag_disable_thread_suspension"></a><dl>
<dt>**WER_FAULT_REPORTING_FLAG_DISABLE_THREAD_SUSPENSION**</dt>
</dl>
</td>
<td width="60%">
Do not suspend the process threads before reporting the error.

</td>
</tr>
<tr>
<td width="40%"><a id="WER_FAULT_REPORTING_FLAG_NOHEAP"></a><a id="wer_fault_reporting_flag_noheap"></a><dl>
<dt>**WER_FAULT_REPORTING_FLAG_NOHEAP**</dt>
</dl>
</td>
<td width="60%">
Do not collect heap information in the event of an application crash or non-response.

</td>
</tr>
<tr>
<td width="40%"><a id="WER_FAULT_REPORTING_FLAG_QUEUE"></a><a id="wer_fault_reporting_flag_queue"></a><dl>
<dt>**WER_FAULT_REPORTING_FLAG_QUEUE**</dt>
</dl>
</td>
<td width="60%">
Queue critical reports.

</td>
</tr>
<tr>
<td width="40%"><a id="WER_FAULT_REPORTING_FLAG_QUEUE_UPLOAD"></a><a id="wer_fault_reporting_flag_queue_upload"></a><dl>
<dt>**WER_FAULT_REPORTING_FLAG_QUEUE_UPLOAD**</dt>
</dl>
</td>
<td width="60%">
Queue critical reports and upload from the queue.

</td>
</tr>
<tr>
<td width="40%"><a id="WER_FAULT_REPORTING_ALWAYS_SHOW_UI"></a><a id="wer_fault_reporting_always_show_ui"></a><dl>
<dt>**WER_FAULT_REPORTING_ALWAYS_SHOW_UI**</dt>
</dl>
</td>
<td width="60%">
Always show error reporting UI for this process. This is applicable for interactive applications only.

</td>
</tr>
</table>

## -returns

This function returns **S_OK** on success or an error code on failure.

## -see-also




<a href="/windows/desktop/api/werapi/nf-werapi-wergetflags">WerGetFlags</a>



[Windows Error Reporting](/windows/desktop/wer)