---
UID: NF:mfapi.MFPutWaitingWorkItem
title: MFPutWaitingWorkItem function
author: windows-driver-content
description: Queues a work item that waits for an event to be signaled.
old-location: mf\mfputwaitingworkitem.htm
old-project: medfound
ms.assetid: BBD80C60-E42F-4B3B-96E3-E01058A27DB8
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: MFPutWaitingWorkItem, MFPutWaitingWorkItem function [Media Foundation], mf.mfputwaitingworkitem, mfapi/MFPutWaitingWorkItem, mfplat/MFPutWaitingWorkItem
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_CUSTOM_DECODE_UNIT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	mfplat.dll
api_name:
-	MFPutWaitingWorkItem
product: Windows
targetos: Windows
req.lib: 
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFPutWaitingWorkItem function


## -description


Queues a work item that waits for an event to be signaled.


## -parameters




### -param hEvent [in]

A handle to an event object. To create an event object, call <a href="https://msdn.microsoft.com/1f6d946e-c74c-4599-ac3d-b709216a0900">CreateEvent</a> or <a href="https://msdn.microsoft.com/402a721d-8338-4df1-ba0b-074f868a1731">CreateEventEx</a>.


### -param Priority [in]

The priority of the work item. Work items are performed in order of priority.


### -param pResult [in]

A pointer to the <a href="https://msdn.microsoft.com/8c95b1de-8974-445c-8070-41552ea83e53">IMFAsyncResult</a> interface of an asynchronous result object. To create the result object, call <a href="https://msdn.microsoft.com/6ff773a9-961e-4a5e-ad37-46234022c575">MFCreateAsyncResult</a>.


### -param pKey [out]

Receives a key that can be used to cancel the wait. To cancel the wait, call <a href="https://msdn.microsoft.com/a24fae61-30c8-4aca-b067-22b99f904fd8">MFCancelWorkItem</a> and pass this key in the <i>Key</i> parameter.

This parameter can be <b>NULL</b>.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function enables a component to wait for an event without blocking the current thread. 

The function puts a work item on the specified work queue. This work item waits for the event given in <i>hEvent</i> to be signaled. When the event is signaled, the work item invokes a callback. (The callback is contained in the result object given in <i>pResult</i>. For more information, see <a href="https://msdn.microsoft.com/6ff773a9-961e-4a5e-ad37-46234022c575">MFCreateAsyncResult</a>).

The work item is dispatched on a work queue by the <a href="https://msdn.microsoft.com/374dd139-d3e7-45d0-a7d3-1187b928ef57">IMFAsyncCallback::GetParameters</a> method of the callback. The work queue can be any of the following:

<ul>
<li>The default work queue (<b>MFASYNC_CALLBACK_QUEUE_STANDARD</b>).</li>
<li>The platform multithreaded queue (<b>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</b>).</li>
<li>A multithreaded queue returned by the <a href="https://msdn.microsoft.com/1E3AA1EE-83A4-42DE-961E-D93A34CE80CF">MFLockSharedWorkQueue</a>  function.</li>
<li>A serial queue created by the <a href="https://msdn.microsoft.com/45198662-C861-49A5-8962-DC256A671350">MFAllocateSerialWorkQueue</a> function.</li>
</ul>
Do not use any of the following work queues: <b>MFASYNC_CALLBACK_QUEUE_IO</b>, <b>MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION</b>, <b>MFASYNC_CALLBACK_QUEUE_RT</b>, or <b>MFASYNC_CALLBACK_QUEUE_TIMER</b>.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/9E2A1D94-BF82-488E-8297-D524683ABE17">Work Queue and Threading Improvements</a>



<a href="https://msdn.microsoft.com/f886d096-b1f5-42e4-8888-501b58bffd50">Work Queues</a>
 

 

