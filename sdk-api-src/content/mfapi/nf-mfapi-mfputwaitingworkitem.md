---
UID: NF:mfapi.MFPutWaitingWorkItem
title: MFPutWaitingWorkItem function (mfapi.h)
description: Queues a work item that waits for an event to be signaled. (MFPutWaitingWorkItem)
helpviewer_keywords: ["MFPutWaitingWorkItem","MFPutWaitingWorkItem function [Media Foundation]","mf.mfputwaitingworkitem","mfapi/MFPutWaitingWorkItem","mfplat/MFPutWaitingWorkItem"]
old-location: mf\mfputwaitingworkitem.htm
tech.root: mf
ms.assetid: BBD80C60-E42F-4B3B-96E3-E01058A27DB8
ms.date: 12/05/2018
ms.keywords: MFPutWaitingWorkItem, MFPutWaitingWorkItem function [Media Foundation], mf.mfputwaitingworkitem, mfapi/MFPutWaitingWorkItem, mfplat/MFPutWaitingWorkItem
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
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFPutWaitingWorkItem
 - mfapi/MFPutWaitingWorkItem
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
 - MFPutWaitingWorkItem
---

# MFPutWaitingWorkItem function


## -description

Queues a work item that waits for an event to be signaled.

## -parameters

### -param hEvent [in]

A handle to an event object. To create an event object, call <a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a> or <a href="/windows/desktop/api/synchapi/nf-synchapi-createeventexa">CreateEventEx</a>.

### -param Priority [in]

The priority of the work item. Work items are performed in order of priority.

### -param pResult [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult">IMFAsyncResult</a> interface of an asynchronous result object. To create the result object, call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult">MFCreateAsyncResult</a>.

### -param pKey [out]

Receives a key that can be used to cancel the wait. To cancel the wait, call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcancelworkitem">MFCancelWorkItem</a> and pass this key in the <i>Key</i> parameter.

This parameter can be <b>NULL</b>.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function enables a component to wait for an event without blocking the current thread. 

The function puts a work item on the specified work queue. This work item waits for the event given in <i>hEvent</i> to be signaled. When the event is signaled, the work item invokes a callback. (The callback is contained in the result object given in <i>pResult</i>. For more information, see <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult">MFCreateAsyncResult</a>).

The work item is dispatched on a work queue by the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-getparameters">IMFAsyncCallback::GetParameters</a> method of the callback. The work queue can be any of the following:

<ul>
<li>The default work queue (<b>MFASYNC_CALLBACK_QUEUE_STANDARD</b>).</li>
<li>The platform multithreaded queue (<b>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</b>).</li>
<li>A multithreaded queue returned by the <a href="/windows/desktop/api/mfapi/nf-mfapi-mflocksharedworkqueue">MFLockSharedWorkQueue</a>  function.</li>
<li>A serial queue created by the <a href="/windows/desktop/api/mfapi/nf-mfapi-mfallocateserialworkqueue">MFAllocateSerialWorkQueue</a> function.</li>
</ul>
Do not use any of the following work queues: <b>MFASYNC_CALLBACK_QUEUE_IO</b>, <b>MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION</b>, <b>MFASYNC_CALLBACK_QUEUE_RT</b>, or <b>MFASYNC_CALLBACK_QUEUE_TIMER</b>.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/media-foundation-work-queue-and-threading-improvements">Work Queue and Threading Improvements</a>



<a href="/windows/desktop/medfound/work-queues">Work Queues</a>
