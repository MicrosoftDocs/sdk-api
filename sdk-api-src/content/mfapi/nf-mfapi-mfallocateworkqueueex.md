---
UID: NF:mfapi.MFAllocateWorkQueueEx
title: MFAllocateWorkQueueEx function (mfapi.h)
description: Creates a new work queue. (MFAllocateWorkQueueEx)
helpviewer_keywords: ["MFAllocateWorkQueueEx","MFAllocateWorkQueueEx function [Media Foundation]","MF_MULTITHREADED_WORKQUEUE","MF_STANDARD_WORKQUEUE","MF_WINDOW_WORKQUEUE","mf.mfallocateworkqueueex","mfapi/MFAllocateWorkQueueEx"]
old-location: mf\mfallocateworkqueueex.htm
tech.root: mf
ms.assetid: 422b8bc2-0616-4f7f-9908-775940f8c1ab
ms.date: 12/05/2018
ms.keywords: MFAllocateWorkQueueEx, MFAllocateWorkQueueEx function [Media Foundation], MF_MULTITHREADED_WORKQUEUE, MF_STANDARD_WORKQUEUE, MF_WINDOW_WORKQUEUE, mf.mfallocateworkqueueex, mfapi/MFAllocateWorkQueueEx
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update Supplement for Windows Vista [desktop apps only]
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
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFAllocateWorkQueueEx
 - mfapi/MFAllocateWorkQueueEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFAllocateWorkQueueEx
---

# MFAllocateWorkQueueEx function


## -description

Creates a new work queue. This function extends the capabilities of the  <a href="/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue">MFAllocateWorkQueue</a> function by making it possible to create a  work queue that has a message loop.

## -parameters

### -param WorkQueueType [in]

A member of the <a href="/windows/desktop/api/mfapi/ne-mfapi-mfasync_workqueue_type">MFASYNC_WORKQUEUE_TYPE</a> enumeration, specifying the type of work queue to create.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MF_MULTITHREADED_WORKQUEUE"></a><a id="mf_multithreaded_workqueue"></a><dl>
<dt><b>MF_MULTITHREADED_WORKQUEUE</b></dt>
</dl>
</td>
<td width="60%">
Create a multithreaded work queue. Generally, applications should not create private multithreaded queues. Use the platform multithreaded queues instead. For more information, see <a href="/windows/desktop/medfound/media-foundation-work-queue-and-threading-improvements">Work Queue and Threading Improvements</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_STANDARD_WORKQUEUE"></a><a id="mf_standard_workqueue"></a><dl>
<dt><b>MF_STANDARD_WORKQUEUE</b></dt>
</dl>
</td>
<td width="60%">
Create a work queue without a message loop. Using this flag is equivalent to calling <a href="/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue">MFAllocateWorkQueue</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_WINDOW_WORKQUEUE"></a><a id="mf_window_workqueue"></a><dl>
<dt><b>MF_WINDOW_WORKQUEUE</b></dt>
</dl>
</td>
<td width="60%">
Create a work queue with a message loop. The thread that dispatches the work items for this queue will also call <a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a> and <a href="/windows/desktop/api/winuser/nf-winuser-dispatchmessage">DispatchMessage</a>. Use this option if your callback performs any actions that require a message loop.

</td>
</tr>
</table>

### -param pdwWorkQueue [out]

Receives an identifier for the work queue that was created.

## -returns

The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The application exceeded the maximum number of work queues.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The application did not call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfstartup">MFStartup</a>, or the application has already called <a href="/windows/desktop/api/mfapi/nf-mfapi-mfshutdown">MFShutdown</a>.

</td>
</tr>
</table>

## -remarks

When you are done using the work queue, call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfunlockworkqueue">MFUnlockWorkQueue</a>.

The <a href="/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue">MFAllocateWorkQueue</a> function is equivalent to calling <b>MFAllocateWorkQueueEx</b> with the value MF_STANDARD_WORKQUEUE for the <i>WorkQueueType</i> parameter.

This function is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.

## -see-also

<a href="/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem">MFPutWorkItem</a>



<a href="/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex">MFPutWorkItemEx</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/work-queues">Work Queues</a>
