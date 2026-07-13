---
UID: NF:dispatcherqueue.CreateDispatcherQueueController
title: CreateDispatcherQueueController function (dispatcherqueue.h)
description: Creates a DispatcherQueueController. Use the created DispatcherQueueController to create and manage the lifetime of a DispatcherQueue to run queued tasks in priority order on the dispatcher queue's thread.
helpviewer_keywords: ["CreateDispatcherQueueController","CreateDispatcherQueueController function","base.createdispatcherqueuecontroller","dispatcherqueue/CreateDispatcherQueueController"]
old-location: base\createdispatcherqueuecontroller.htm
tech.root: backup
ms.assetid: 750097BB-C4D1-4579-9353-582124D5CE3B
ms.date: 12/05/2018
ms.keywords: CreateDispatcherQueueController, CreateDispatcherQueueController function, base.createdispatcherqueuecontroller, dispatcherqueue/CreateDispatcherQueueController
req.header: dispatcherqueue.h
req.include-header: 
req.target-type: Windows
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
req.lib: CoreMessaging.lib
req.dll: CoreMessaging.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateDispatcherQueueController
 - dispatcherqueue/CreateDispatcherQueueController
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - CoreMessaging.dll
api_name:
 - CreateDispatcherQueueController
---

## -description

Creates a <a href="/uwp/api/windows.system.dispatcherqueuecontroller">DispatcherQueueController</a>. Use the created <a href="/uwp/api/windows.system.dispatcherqueuecontroller">DispatcherQueueController</a> to create and manage the lifetime of a <a href="/uwp/api/windows.system.dispatcherqueue">DispatcherQueue</a> to run queued tasks in priority order on the dispatcher queue's thread.

## -parameters

### -param options [in]

The threading affinity and type of COM apartment for the created <a href="/uwp/api/windows.system.dispatcherqueuecontroller">DispatcherQueueController</a>. See remarks for details.

### -param dispatcherQueueController [out]

The created dispatcher queue controller. 

<div class="alert"><b>Important</b>  The <a href="/uwp/api/windows.system.dispatcherqueuecontroller">DispatcherQueueController</a> is a WinRT object.</div>
<div> </div>

## -returns

<b>S_OK</b> for success; otherwise a failure code.

## -remarks

Introduced in Windows 10, version 1709.

If <i>options.threadType</i> is <b>DQTYPE_THREAD_DEDICATED</b>, then this function
creates a thread, initializes it with the specified COM apartment,
and associates a <a href="/uwp/api/windows.system.dispatcherqueue">DispatcherQueue</a> with that thread.
The dispatcher queue event loop runs on the new dedicated thread until the dispatcher queue is explicitly shut down.
To avoid thread and memory leaks,
call <a href="/uwp/api/windows.system.dispatcherqueuecontroller.shutdownqueueasync">DispatcherQueueController.ShutdownQueueAsync</a>
when you are finished with the dispatcher queue.

If <i>options.threadType</i> is <b>DQTYPE_THREAD_CURRENT</b>, then a
<a href="/uwp/api/windows.system.dispatcherqueue">DispatcherQueue</a> is created and associated with the current thread.
An error results if there is already a <b>DispatcherQueue</b> associated with the current thread.
The current thread must pump messages to allow the dispatcher queue to dispatch tasks.
Before the current thread exits, it must call
<a href="/uwp/api/windows.system.dispatcherqueuecontroller.shutdownqueueasync">DispatcherQueueController.ShutdownQueueAsync</a>,
and continue pumping messages until the <b>IAsyncAction</b> completes.

This call does not return until the <a href="/uwp/api/windows.system.dispatcherqueuecontroller">DispatcherQueueController</a> and new thread (if any) are created.

<div class="alert"><b>Important</b>  The <a href="/uwp/api/windows.system.dispatcherqueuecontroller">DispatcherQueueController</a>, and its associated <a href="/uwp/api/windows.system.dispatcherqueue">DispatcherQueue</a>, are WinRT objects. See their documentation for usage details.</div>
<div> </div>

## -see-also

<a href="/uwp/api/windows.system.dispatcherqueue">DispatcherQueue</a>



<a href="/uwp/api/windows.system.dispatcherqueuecontroller">DispatcherQueueController</a>
