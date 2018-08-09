---
UID: NF:winnt.InterlockedDecrement16
title: InterlockedDecrement16 function
author: windows-sdk-content
description: Decrements (decreases by one) the value of the specified 16-bit variable as an atomic operation.
old-location: base\interlockeddecrement16.htm
old-project: sync
ms.assetid: 64fbfe37-fce5-4d96-aecb-3850d1edd34e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: InterlockedDecrement16, InterlockedDecrement16 function, base.interlockeddecrement16, winnt/InterlockedDecrement16
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winnt.h
req.include-header: Windows.h
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
tech.root: 
req.typenames: TRANSACTION_OUTCOME
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - InterlockedDecrement16
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# InterlockedDecrement16 function


## -description


Decrements (decreases by one) the value of the specified 16-bit variable as an atomic operation.

To operate on 32-bit values, use the <a href="https://msdn.microsoft.com/library/windows/hardware/ff547871">InterlockedDecrement</a> function.

To operate on 64-bit values, use the <a href="https://msdn.microsoft.com/073b42ba-90dd-48a1-9661-9b1686c09561">InterlockedDecrement64</a> function.


## -parameters




### -param Addend [in, out]

A pointer to the variable to be decremented.


## -returns



The function returns the resulting decremented value.
      
     




## -remarks



The variable pointed to by the <i>Addend</i> parameter must be aligned on a 16-bit boundary; otherwise, this function will behave unpredictably on multiprocessor x86 systems and any non-x86 systems. See <b>_aligned_malloc</b>.

The interlocked functions provide a simple mechanism for synchronizing access to a variable that is shared by multiple threads. This function is atomic with respect to calls to other interlocked functions.

This function is implemented using a compiler intrinsic where possible. For more information, see the WinBase.h header file and <a href="5268fce3-86b5-4b2b-b96c-2e531a3fb9b5">_InterlockedDecrement16</a>.

This function generates a full memory barrier (or fence) to ensure that memory operations are completed in order.

<div class="alert"><b>Note</b>  This function is supported on Windows RT-based systems.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/729c0e68-ef52-4d6c-b771-a89043a937e6">Interlocked Variable Access</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff547871">InterlockedDecrement</a>



<a href="https://msdn.microsoft.com/06a24299-827c-4066-9846-4f3b3f2cce2b">InterlockedDecrement16Acquire</a>



<a href="https://msdn.microsoft.com/02dc980e-69bc-41d0-bdac-9f87962a5bde">InterlockedDecrement16NoFence</a>



<a href="https://msdn.microsoft.com/d6b87ae2-69f7-4d83-bb8e-bcce36c408bb">InterlockedDecrement16Release</a>



<a href="https://msdn.microsoft.com/073b42ba-90dd-48a1-9661-9b1686c09561">InterlockedDecrement64</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff547875">InterlockedDecrementAcquire</a>



<a href="https://msdn.microsoft.com/cc2de6b6-4a0c-410e-82c9-3064f471b16b">InterlockedDecrementAcquire64</a>



<a href="https://msdn.microsoft.com/8cebfe9a-795c-4934-8064-e2297476e351">InterlockedDecrementNoFence</a>



<a href="https://msdn.microsoft.com/d98d5a09-ac36-4d25-ae04-f1a16b628b6a">InterlockedDecrementNoFence64</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff547883">InterlockedDecrementRelease</a>



<a href="https://msdn.microsoft.com/1ad161d9-0252-420f-8c58-2ea8fbf6a117">InterlockedDecrementRelease64</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>
 

 

