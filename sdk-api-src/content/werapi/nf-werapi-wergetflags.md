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

# WerGetFlags function


## -description


Retrieves the fault reporting settings for the specified process.


## -parameters




### -param hProcess [in]

A handle to the process. This handle must have the PROCESS_VM_READ or PROCESS_QUERY_INFORMATION access right.


### -param pdwFlags [out]

This parameter can contain one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WER_FAULT_REPORTING_FLAG_DISABLE_THREAD_SUSPENSION"></a><a id="wer_fault_reporting_flag_disable_thread_suspension"></a><dl>
<dt><b>WER_FAULT_REPORTING_FLAG_DISABLE_THREAD_SUSPENSION</b></dt>
</dl>
</td>
<td width="60%">
Do not suspend the process threads before reporting the error.

</td>
</tr>
<tr>
<td width="40%"><a id="WER_FAULT_REPORTING_FLAG_NOHEAP"></a><a id="wer_fault_reporting_flag_noheap"></a><dl>
<dt><b>WER_FAULT_REPORTING_FLAG_NOHEAP</b></dt>
</dl>
</td>
<td width="60%">
Do not collect heap information in the event of an application crash or non-response.

</td>
</tr>
<tr>
<td width="40%"><a id="WER_FAULT_REPORTING_FLAG_QUEUE"></a><a id="wer_fault_reporting_flag_queue"></a><dl>
<dt><b>WER_FAULT_REPORTING_FLAG_QUEUE</b></dt>
</dl>
</td>
<td width="60%">
Queue critical reports for the specified process. This does not show any UI.

</td>
</tr>
<tr>
<td width="40%"><a id="WER_FAULT_REPORTING_FLAG_QUEUE_UPLOAD"></a><a id="wer_fault_reporting_flag_queue_upload"></a><dl>
<dt><b>WER_FAULT_REPORTING_FLAG_QUEUE_UPLOAD</b></dt>
</dl>
</td>
<td width="60%">
Queue critical reports and upload from the queue.

</td>
</tr>
<tr>
<td width="40%"><a id="WER_FAULT_REPORTING_ALWAYS_SHOW_UI"></a><a id="wer_fault_reporting_always_show_ui"></a><dl>
<dt><b>WER_FAULT_REPORTING_ALWAYS_SHOW_UI</b></dt>
</dl>
</td>
<td width="60%">
Always show error reporting UI for this process. This is applicable for interactive applications only.

</td>
</tr>
</table>
 


## -returns



This function returns <b>S_OK</b> on success or an error code on failure.




## -see-also




<a href="https://msdn.microsoft.com/4e28f379-5793-4d76-898e-d87a0291c034">WER Functions</a>



<a href="https://msdn.microsoft.com/2a71203f-3a08-461f-a230-e3fee00d9d99">WerSetFlags</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/jj242491">Windows Error Reporting</a>
 

 

