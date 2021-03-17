---
UID: NF:dispatcherqueue.CreateDispatcherQueueController
title: CreateDispatcherQueueController function (dispatcherqueue.h)
description: Creates a DispatcherQueueController on the caller's thread. Use the created DispatcherQueueController to create and manage the lifetime of a DispatcherQueue to run queued tasks in priority order on the Dispatcher queue's thread.
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

# CreateDispatcherQueueController function


## -description

Creates a <a href="/uwp/api/windows.system.dispatcherqueuecontroller">DispatcherQueueController</a> on the caller's thread. Use the created <a href="/uwp/api/windows.system.dispatcherqueuecontroller">DispatcherQueueController</a> to create and manage the lifetime of a <a href="/uwp/api/windows.system.dispatcherqueue">DispatcherQueue</a> to run queued tasks in priority order on the Dispatcher queue's thread.

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

 If  <i>options.threadType</i> is <b>DQTYPE_THREAD_DEDICATED</b>, then this function  creates the dedicated thread and then creates the  <a href="/uwp/api/windows.system.dispatcherqueuecontroller">DispatcherQueueController</a> on that thread. The dispatcher queue event loop runs on the new dedicated thread.

An event loop runs asynchronously on a background thread to dispatch
queued task items to the new dedicated thread.

 If <i>options.threadType</i> is  <b>DQTYPE_THREAD_CURRENT</b>, then the <a href="/uwp/api/windows.system.dispatcherqueuecontroller">DispatcherQueueController</a> instance is created on the current thread. An error results if there is already 
a <b>IDispatcherQueueController</b> on the current thread. If you create a dispatcher queue on the current thread, ensure that there is a message pump running on the current thread so that the dispatcher queue can use it to dispatch tasks.

This call does not return until the new thread and <a href="/uwp/api/windows.system.dispatcherqueuecontroller">DispatcherQueueController</a> are created. The new thread will be initialized using the specified COM apartment.

<div class="alert"><b>Important</b>  The <a href="/uwp/api/windows.system.dispatcherqueuecontroller">DispatcherQueueController</a>, and its associated <a href="/uwp/api/windows.system.dispatcherqueue">DispatcherQueue</a>, are WinRT objects. See their documentation for usage details.</div>
<div> </div>

## -see-also

<a href="/uwp/api/windows.system.dispatcherqueue">DispatcherQueue</a>



<a href="/uwp/api/windows.system.dispatcherqueuecontroller">DispatcherQueueController</a>