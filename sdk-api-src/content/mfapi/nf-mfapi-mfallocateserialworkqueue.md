---
UID: NF:mfapi.MFAllocateSerialWorkQueue
title: MFAllocateSerialWorkQueue function
author: windows-sdk-content
description: Creates a work queue that is guaranteed to serialize work items.
old-location: mf\mfallocateserialworkqueue.htm
tech.root: medfound
ms.assetid: 45198662-C861-49A5-8962-DC256A671350
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MFAllocateSerialWorkQueue, MFAllocateSerialWorkQueue function [Media Foundation], mf.mfallocateserialworkqueue, mfapi/MFAllocateSerialWorkQueue
ms.topic: function
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - MFAllocateSerialWorkQueue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFAllocateSerialWorkQueue function


## -description


Creates a work queue that is guaranteed to serialize work items. The serial work queue wraps an existing multithreaded work queue. The serial work queue enforces a first-in, first-out (FIFO) execution order.


## -parameters




### -param dwWorkQueue [in]

The identifier of an existing work queue. This must be either a multithreaded queue or another serial work queue. Any of the following can be used:

<ul>
<li>The default work queue (<b>MFASYNC_CALLBACK_QUEUE_STANDARD</b>)</li>
<li>The platform multithreaded queue (<b>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</b>)</li>
<li>A multithreaded queue returned by the <a href="https://msdn.microsoft.com/1E3AA1EE-83A4-42DE-961E-D93A34CE80CF">MFLockSharedWorkQueue</a>  function.</li>
<li>A serial queue created by the <b>MFAllocateSerialWorkQueue</b> function.</li>
</ul>

### -param pdwWorkQueue [out]

Receives an identifier for the new serial work queue. Use this identifier when queuing work items.


## -returns



This function can return one of these values.

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

Multithreaded queues use a thread pool, which  can reduce the total number of threads in the pipeline. However, they do not serialize work items. A serial work queue enables the application to get the benefits of the thread pool, without needing to perform manual serialization of its own work items.

<h3><a id="Reply_Mode"></a><a id="reply_mode"></a><a id="REPLY_MODE"></a>Reply Mode</h3>
A serializer queue can also work in "reply" mode. If the caller’s <a href="https://msdn.microsoft.com/374dd139-d3e7-45d0-a7d3-1187b928ef57">IMFAsyncCallback::GetParameters</a> method returns the <b>MFASYNC_REPLY_CALLBACK</b> flag, the serializer queue does not automatically advance to the next work item. Instead, the queue waits for a reply from the caller. The caller signals the reply by invoking the asynchronous result object that the work queue passes to the <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">Invoke</a> method. The following code illustrates how the caller signals the work queue.


```cpp
HRESULT CCallback::Invoke(IMFAsyncResult *pResult)
{
    DoSomeWork();
    
    // Reply to the work queue that you are done.
    MFInvokeCallback(pResult);

    // Note: This call to MFInvokeCallback does not have to occur inside the
    // Invoke method. You could call MFInvokeCallback at a later time. 

    return S_OK;
}
HRESULT CCallback::GetParameters(DWORD *pdwFlags, DWORD *pdwQueue)
{
    *pdwFlags = MFASYNC_REPLY_CALLBACK;
    *pdwQueue = m_QueueId;
    return S_OK;
}

```





## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/9E2A1D94-BF82-488E-8297-D524683ABE17">Work Queue and Threading Improvements</a>
 

 

