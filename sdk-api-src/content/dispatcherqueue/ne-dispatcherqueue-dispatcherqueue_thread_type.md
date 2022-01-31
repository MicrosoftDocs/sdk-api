---
UID: NE:dispatcherqueue.DISPATCHERQUEUE_THREAD_TYPE
title: DISPATCHERQUEUE_THREAD_TYPE (dispatcherqueue.h)
description: Specifies the thread affinity for a new DispatcherQueueController.
helpviewer_keywords: ["DISPATCHERQUEUE_THREAD_TYPE","DISPATCHERQUEUE_THREAD_TYPE enumeration","DQTYPE_THREAD_CURRENT","DQTYPE_THREAD_DEDICATED","base.dispatcherqueue_thread_type","dispatcherqueue/DISPATCHERQUEUE_THREAD_TYPE","dispatcherqueue/DQTYPE_THREAD_CURRENT","dispatcherqueue/DQTYPE_THREAD_DEDICATED"]
old-location: base\dispatcherqueue_thread_type.htm
tech.root: backup
ms.assetid: 72558E7E-0ECB-4641-949F-07C43A6E2507
ms.date: 12/05/2018
ms.keywords: DISPATCHERQUEUE_THREAD_TYPE, DISPATCHERQUEUE_THREAD_TYPE enumeration, DQTYPE_THREAD_CURRENT, DQTYPE_THREAD_DEDICATED, base.dispatcherqueue_thread_type, dispatcherqueue/DISPATCHERQUEUE_THREAD_TYPE, dispatcherqueue/DQTYPE_THREAD_CURRENT, dispatcherqueue/DQTYPE_THREAD_DEDICATED
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DISPATCHERQUEUE_THREAD_TYPE
 - dispatcherqueue/DISPATCHERQUEUE_THREAD_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DispatcherQueue.h
api_name:
 - DISPATCHERQUEUE_THREAD_TYPE
---

# DISPATCHERQUEUE_THREAD_TYPE enumeration


## -description

Specifies the thread affinity for a new <a href="/uwp/api/windows.system.dispatcherqueuecontroller">DispatcherQueueController</a>.

## -enum-fields

### -field DQTYPE_THREAD_DEDICATED:1

 Specifies that the <a href="/uwp/api/windows.system.dispatcherqueuecontroller">DispatcherQueueController</a> be created on a dedicated thread. With this option, <a href="/windows/desktop/api/dispatcherqueue/nf-dispatcherqueue-createdispatcherqueuecontroller">CreateDispatcherQueueController</a> creates a thread, the <a href="/uwp/api/windows.system.dispatcherqueuecontroller">DispatcherQueueController</a> instance, and runs the dispatcher queue event loop on the newly created thread.

### -field DQTYPE_THREAD_CURRENT:2

Specifies that the <a href="/uwp/api/windows.system.dispatcherqueuecontroller">DispatcherQueueController</a> will be created on the caller's thread.

## -remarks

Introduced in Windows 10, version 1709.

## -see-also

<a href="/windows/desktop/api/dispatcherqueue/nf-dispatcherqueue-createdispatcherqueuecontroller">CreateDispatcherQueueController</a>



<a href="/windows/desktop/api/dispatcherqueue/ns-dispatcherqueue-dispatcherqueueoptions">DispatcherQueueOptions</a>
