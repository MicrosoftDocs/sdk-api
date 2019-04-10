---
UID: NF:winnt.InterlockedDecrement64
title: InterlockedDecrement64 function (winnt.h)
author: windows-sdk-content
description: Decrements (decreases by one) the value of the specified 64-bit variable as an atomic operation.
old-location: base\interlockeddecrement64.htm
tech.root: Sync
ms.assetid: 073b42ba-90dd-48a1-9661-9b1686c09561
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: InterlockedDecrement64, InterlockedDecrement64 function, base.interlockeddecrement64, winnt/InterlockedDecrement64
ms.topic: function
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - Winnt.h
api_name:
 - InterlockedDecrement64
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# InterlockedDecrement64 function


## -description


Decrements (decreases by one) the value of the specified 64-bit variable as an atomic operation.

To operate on 32-bit values, use the <a href="https://msdn.microsoft.com/en-us/library/ms683580(v=VS.85).aspx">InterlockedDecrement</a> function.


## -parameters




### -param Addend [in, out]

A pointer to the variable to be decremented.


## -returns



The function returns the resulting decremented value.




## -remarks



The variable pointed to by the <i>Addend</i> parameter must be aligned on a 64-bit boundary; otherwise, this function will behave unpredictably on multiprocessor x86 systems and any non-x86 systems. See <b>_aligned_malloc</b>.

The interlocked functions provide a simple mechanism for synchronizing access to a variable that is shared by multiple threads. This function is atomic with respect to calls to other interlocked functions.

This function is implemented using a compiler intrinsic where possible. For more information, see the WinBase.h header file and <a href="https://msdn.microsoft.com/library/f24ya7ct(v=VS.85).aspx">_InterlockedDecrement64</a>.

This function  generates a full memory barrier (or fence) to ensure that memory operations are completed in order.

<b>Itanium-based systems:  </b>For performance-critical applications, use <a href="https://msdn.microsoft.com/cc2de6b6-4a0c-410e-82c9-3064f471b16b">InterlockedDecrementAcquire64</a> or <a href="https://msdn.microsoft.com/1ad161d9-0252-420f-8c58-2ea8fbf6a117">InterlockedDecrementRelease64</a> instead.

<div class="alert"><b>Note</b>  This function is supported on Windows RT-based systems.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/729c0e68-ef52-4d6c-b771-a89043a937e6">Interlocked Variable Access</a>



<a href="https://msdn.microsoft.com/en-us/library/ms683580(v=VS.85).aspx">InterlockedDecrement</a>



<a href="https://msdn.microsoft.com/64fbfe37-fce5-4d96-aecb-3850d1edd34e">InterlockedDecrement16</a>



<a href="https://msdn.microsoft.com/06a24299-827c-4066-9846-4f3b3f2cce2b">InterlockedDecrement16Acquire</a>



<a href="https://msdn.microsoft.com/02dc980e-69bc-41d0-bdac-9f87962a5bde">InterlockedDecrement16NoFence</a>



<a href="https://msdn.microsoft.com/d6b87ae2-69f7-4d83-bb8e-bcce36c408bb">InterlockedDecrement16Release</a>



<a href="https://msdn.microsoft.com/63af8047-1ccf-4cea-9940-584f34e73dcf">InterlockedDecrementAcquire</a>



<a href="https://msdn.microsoft.com/cc2de6b6-4a0c-410e-82c9-3064f471b16b">InterlockedDecrementAcquire64</a>



<a href="https://msdn.microsoft.com/8cebfe9a-795c-4934-8064-e2297476e351">InterlockedDecrementNoFence</a>



<a href="https://msdn.microsoft.com/d98d5a09-ac36-4d25-ae04-f1a16b628b6a">InterlockedDecrementNoFence64</a>



<a href="https://msdn.microsoft.com/ee5ef016-3d64-4c2d-83f1-47f9ab612836">InterlockedDecrementRelease</a>



<a href="https://msdn.microsoft.com/1ad161d9-0252-420f-8c58-2ea8fbf6a117">InterlockedDecrementRelease64</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>
 

 

