---
UID: NF:synchapi.DeleteSynchronizationBarrier
title: DeleteSynchronizationBarrier function
author: windows-sdk-content
description: Deletes a synchronization barrier.
old-location: base\deletesynchronizationbarrier.htm
tech.root: sync
ms.assetid: 04626b6f-f5f7-4042-9786-7cabd68636ac
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DeleteSynchronizationBarrier, DeleteSynchronizationBarrier function, base.deletesynchronizationbarrier, synchapi/DeleteSynchronizationBarrier
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: synchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Synch-l1-2-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Synch-l1-2-1.dll
 - MinKernelBase.dll
api_name:
 - DeleteSynchronizationBarrier
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DeleteSynchronizationBarrier function


## -description


Deletes a synchronization barrier.


## -parameters




### -param lpBarrier [in, out]

A pointer to the synchronization barrier to delete.


## -returns



The <b>DeleteSynchronizationBarrier</b> function always returns <b>TRUE</b>.




## -remarks



<b>DeleteSynchronizationBarrier</b> releases a synchronization barrier when it is no longer needed. It is safe to call <b>DeleteSynchronizationBarrier</b> immediately after calling <a href="https://msdn.microsoft.com/cd938370-b046-4369-931d-5c7c8db7303a">EnterSynchronizationBarrier</a> because that function ensures that all threads in the barrier have finished using it before allowing the barrier to be released. 

If a synchronization barrier will never be deleted, threads can specify the <b>SYNCHRONIZATION_BARRIER_FLAGS_NO_DELETE</b> flag when they enter the barrier. This flag causes the function to skip the extra work required for deletion safety, which can improve performance. All threads using the barrier must specify this flag; if any thread does not, the flag is ignored. Be careful when using <b>SYNCHRONIZATION_BARRIER_FLAGS_NO_DELETE</b>, because deleting a barrier while this flag is in effect  may result in an invalid handle access and cause one or more threads to become permanently blocked. 




## -see-also




<a href="https://msdn.microsoft.com/cd938370-b046-4369-931d-5c7c8db7303a">EnterSynchronizationBarrier</a>



<a href="https://msdn.microsoft.com/f69934a1-ee1f-4400-ae3e-cb9a19feff93">InitializeSynchronizationBarrier</a>



<a href="https://msdn.microsoft.com/3A76E6F7-C38B-4843-9496-36F3C78B700C">Synchronization Barriers</a>
 

 

