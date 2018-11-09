---
UID: NF:mfapi.MFBeginUnregisterWorkQueueWithMMCSS
title: MFBeginUnregisterWorkQueueWithMMCSS function
author: windows-sdk-content
description: Unregisters a work queue from a Multimedia Class Scheduler Service (MMCSS) task.
old-location: mf\mfbeginunregisterworkqueuewithmmcss.htm
tech.root: medfound
ms.assetid: e164785f-9899-45f0-805f-b091508e35aa
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: MFBeginUnregisterWorkQueueWithMMCSS, MFBeginUnregisterWorkQueueWithMMCSS function [Media Foundation], e164785f-9899-45f0-805f-b091508e35aa, mf.mfbeginunregisterworkqueuewithmmcss, mfapi/MFBeginUnregisterWorkQueueWithMMCSS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfapi.h
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
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFBeginUnregisterWorkQueueWithMMCSS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFBeginUnregisterWorkQueueWithMMCSS function


## -description



Unregisters a work queue from a Multimedia Class Scheduler Service (MMCSS) task.




## -parameters




### -param dwWorkQueueId [in]

The identifier of the work queue.  For private work queues, the identifier is returned by the <a href="https://msdn.microsoft.com/8def4375-919c-4619-9484-9ce2708a3886">MFAllocateWorkQueue</a> function. For platform work queues, see <a href="https://msdn.microsoft.com/c769f876-83ca-4b04-a054-22fa7146310e">Work Queue Identifiers</a>.


### -param pDoneCallback [in]

Pointer to the <a href="https://msdn.microsoft.com/7edff985-da59-4cc0-96de-1a92e03a7d41">IMFAsyncCallback</a> interface of a callback object. The caller must implement this interface.


### -param pDoneState [in]

Pointer to the <b>IUnknown</b> interface of a state object, defined by the caller. This parameter can be <b>NULL</b>. You can use this object to hold state information. The object is returned to the caller when the callback is invoked.


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
</table>
 




## -remarks



This function unregisters a work queue that was associated with an MMCSS class through the <a href="https://msdn.microsoft.com/9bcc6ab3-b7da-4b32-a868-c16f83ce20ca">MFBeginRegisterWorkQueueWithMMCSS</a> function.

This function is asynchronous. When the operation completes, the callback object's <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">IMFAsyncCallback::Invoke</a> method is called. At that point, the application should call <a href="https://msdn.microsoft.com/eca38d5d-9ca3-442e-80ca-96d8927178a1">MFEndUnregisterWorkQueueWithMMCSS</a> to complete the asynchronous request.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/f886d096-b1f5-42e4-8888-501b58bffd50">Work Queues</a>
 

 

