---
UID: NF:mfapi.MFAllocateWorkQueueEx
title: MFAllocateWorkQueueEx function
author: windows-sdk-content
description: Creates a new work queue.
old-location: mf\mfallocateworkqueueex.htm
old-project: medfound
ms.assetid: 422b8bc2-0616-4f7f-9908-775940f8c1ab
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: MFAllocateWorkQueueEx, MFAllocateWorkQueueEx function [Media Foundation], MF_MULTITHREADED_WORKQUEUE, MF_STANDARD_WORKQUEUE, MF_WINDOW_WORKQUEUE, mf.mfallocateworkqueueex, mfapi/MFAllocateWorkQueueEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: MF_CUSTOM_DECODE_UNIT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFAllocateWorkQueueEx
product: Windows
targetos: Windows
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFAllocateWorkQueueEx function


## -description


Creates a new work queue. This function extends the capabilities of the  <a href="https://msdn.microsoft.com/8def4375-919c-4619-9484-9ce2708a3886">MFAllocateWorkQueue</a> function by making it possible to create a  work queue that has a message loop.


## -parameters




### -param WorkQueueType [in]

A member of the <a href="https://msdn.microsoft.com/a3627dbc-1794-4e2e-b7ed-869ed50ca893">MFASYNC_WORKQUEUE_TYPE</a> enumeration, specifying the type of work queue to create.

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
Create a multithreaded work queue. Generally, applications should not create private multithreaded queues. Use the platform multithreaded queues instead. For more information, see <a href="https://msdn.microsoft.com/9E2A1D94-BF82-488E-8297-D524683ABE17">Work Queue and Threading Improvements</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_STANDARD_WORKQUEUE"></a><a id="mf_standard_workqueue"></a><dl>
<dt><b>MF_STANDARD_WORKQUEUE</b></dt>
</dl>
</td>
<td width="60%">
Create a work queue without a message loop. Using this flag is equivalent to calling <a href="https://msdn.microsoft.com/8def4375-919c-4619-9484-9ce2708a3886">MFAllocateWorkQueue</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_WINDOW_WORKQUEUE"></a><a id="mf_window_workqueue"></a><dl>
<dt><b>MF_WINDOW_WORKQUEUE</b></dt>
</dl>
</td>
<td width="60%">
Create a work queue with a message loop. The thread that dispatches the work items for this queue will also call <a href="https://msdn.microsoft.com/b9f5baa4-8166-4d6e-b416-df023aed9bad">PeekMessage</a> and <a href="https://msdn.microsoft.com/6d5e2d1d-dcd2-48ce-a8ba-99bd5dbdfb21">DispatchMessage</a>. Use this option if your callback performs any actions that require a message loop.

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
The application did not call <a href="https://msdn.microsoft.com/b4472e40-3681-4b26-9385-4df7bf19c2d8">MFStartup</a>, or the application has already called <a href="https://msdn.microsoft.com/10be2361-b5b4-4c10-92a1-527ca22c74e4">MFShutdown</a>.

</td>
</tr>
</table>
 




## -remarks



When you are done using the work queue, call <a href="https://msdn.microsoft.com/bbc22fa7-b4d7-47b2-b065-099fbb2ed092">MFUnlockWorkQueue</a>.

The <a href="https://msdn.microsoft.com/8def4375-919c-4619-9484-9ce2708a3886">MFAllocateWorkQueue</a> function is equivalent to calling <b>MFAllocateWorkQueueEx</b> with the value MF_STANDARD_WORKQUEUE for the <i>WorkQueueType</i> parameter.

This function is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.




## -see-also




<a href="https://msdn.microsoft.com/b0233589-2a55-4803-9dcb-85d757734dee">MFPutWorkItem</a>



<a href="https://msdn.microsoft.com/67b4f7c6-0d49-4ed0-9bc3-e583451884af">MFPutWorkItemEx</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/f886d096-b1f5-42e4-8888-501b58bffd50">Work Queues</a>
 

 

