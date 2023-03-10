---
UID: NF:mfidl.IMFRealTimeClientEx.RegisterThreadsEx
title: IMFRealTimeClientEx::RegisterThreadsEx (mfidl.h)
description: Notifies the object to register its worker threads with the Multimedia Class Scheduler Service (MMCSS). (IMFRealTimeClientEx.RegisterThreadsEx)
helpviewer_keywords: ["IMFRealTimeClientEx interface [Media Foundation]","RegisterThreadsEx method","IMFRealTimeClientEx.RegisterThreadsEx","IMFRealTimeClientEx::RegisterThreadsEx","RegisterThreadsEx","RegisterThreadsEx method [Media Foundation]","RegisterThreadsEx method [Media Foundation]","IMFRealTimeClientEx interface","mf.imfrealtimeclientex_registerthreadsex","mfidl/IMFRealTimeClientEx::RegisterThreadsEx"]
old-location: mf\imfrealtimeclientex_registerthreadsex.htm
tech.root: mf
ms.assetid: 45E3121A-F6FD-49C7-B147-5317C045DE35
ms.date: 12/05/2018
ms.keywords: IMFRealTimeClientEx interface [Media Foundation],RegisterThreadsEx method, IMFRealTimeClientEx.RegisterThreadsEx, IMFRealTimeClientEx::RegisterThreadsEx, RegisterThreadsEx, RegisterThreadsEx method [Media Foundation], RegisterThreadsEx method [Media Foundation],IMFRealTimeClientEx interface, mf.imfrealtimeclientex_registerthreadsex, mfidl/IMFRealTimeClientEx::RegisterThreadsEx
req.header: mfidl.h
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFRealTimeClientEx::RegisterThreadsEx
 - mfidl/IMFRealTimeClientEx::RegisterThreadsEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFRealTimeClientEx.RegisterThreadsEx
---

# IMFRealTimeClientEx::RegisterThreadsEx


## -description

Notifies the object to register its worker threads with the Multimedia Class Scheduler Service (MMCSS).

## -parameters

### -param pdwTaskIndex [in, out]

The MMCSS task identifier. If the value is zero on input,  the object should create a new MCCSS task group. See Remarks.

### -param wszClassName [in]

The name of the MMCSS task.

### -param lBasePriority [in]

The base priority of the thread.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the object does not create worker threads, the method should simply return S_OK and take no further action. 

Otherwise, if the value of <code>*pdwTaskIndex</code> is zero on input, the object should perform the following steps:

<ol>
<li>A single worker thread calls <a href="/windows/desktop/api/avrt/nf-avrt-avsetmmthreadcharacteristicsa">AvSetMmThreadCharacteristics</a> to create a new MMCSS task identifier. Store this value.</li>
<li>Any additional worker threads call <a href="/windows/desktop/api/avrt/nf-avrt-avsetmmthreadcharacteristicsa">AvSetMmThreadCharacteristics</a> using the new task identifier.</li>
<li>Return the new task identifier to the caller, by setting <code>*pdwTaskIndex</code> equal to the task identifier.</li>
</ol>
If the value of <code>*pdwTaskIndex</code> is nonzero on input, the parameter contains an existing MMCSS task identifier. In that case, all worker threads of the object should register themselves for that task by calling <a href="/windows/desktop/api/avrt/nf-avrt-avsetmmthreadcharacteristicsa">AvSetMmThreadCharacteristics</a>.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex">IMFRealTimeClientEx</a>



<a href="/windows/desktop/medfound/media-foundation-work-queue-and-threading-improvements">Work Queue and Threading Improvements</a>
