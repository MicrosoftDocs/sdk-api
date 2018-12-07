---
UID: NE:dispatcherqueue.DISPATCHERQUEUE_THREAD_TYPE
title: DISPATCHERQUEUE_THREAD_TYPE
author: windows-sdk-content
description: Specifies the thread affinity for a new DispatcherQueueController.
old-location: base\dispatcherqueue_thread_type.htm
tech.root: procthread
ms.assetid: 72558E7E-0ECB-4641-949F-07C43A6E2507
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DISPATCHERQUEUE_THREAD_TYPE, DISPATCHERQUEUE_THREAD_TYPE enumeration, DQTYPE_THREAD_CURRENT, DQTYPE_THREAD_DEDICATED, base.dispatcherqueue_thread_type, dispatcherqueue/DISPATCHERQUEUE_THREAD_TYPE, dispatcherqueue/DQTYPE_THREAD_CURRENT, dispatcherqueue/DQTYPE_THREAD_DEDICATED
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DispatcherQueue.h
api_name:
 - DISPATCHERQUEUE_THREAD_TYPE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DISPATCHERQUEUE_THREAD_TYPE enumeration


## -description


Specifies the thread affinity for a new <a href="https://docs.microsoft.com/uwp/api/windows.system.dispatcherqueuecontroller">DispatcherQueueController</a>.


## -enum-fields




### -field DQTYPE_THREAD_DEDICATED

 Specifies that the <a href="https://docs.microsoft.com/uwp/api/windows.system.dispatcherqueuecontroller">DispatcherQueueController</a> be created on a dedicated thread. With this option, <a href="https://msdn.microsoft.com/750097BB-C4D1-4579-9353-582124D5CE3B">CreateDispatcherQueueController</a> creates a thread, the <a href="https://docs.microsoft.com/uwp/api/windows.system.dispatcherqueuecontroller">DispatcherQueueController</a> instance, and runs the dispatcher queue event loop on the newly created thread.


### -field DQTYPE_THREAD_CURRENT

Specifies that the <a href="https://docs.microsoft.com/uwp/api/windows.system.dispatcherqueuecontroller">DispatcherQueueController</a> will be created on the caller's thread.


## -remarks



Introduced in Windows 10, version 1709.




## -see-also




<a href="https://msdn.microsoft.com/750097BB-C4D1-4579-9353-582124D5CE3B">CreateDispatcherQueueController</a>



<a href="https://msdn.microsoft.com/F9AF7DDE-13EB-43DB-BAD5-61A6ABD9307D">DispatcherQueueOptions</a>
 

 

