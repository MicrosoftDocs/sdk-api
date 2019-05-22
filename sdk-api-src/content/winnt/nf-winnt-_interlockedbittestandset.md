---
UID: NF:winnt._interlockedbittestandset
title: _interlockedbittestandset function (winnt.h)
author: windows-sdk-content
description: Tests the specified bit of the specified LONG value and sets it to 1. The operation is atomic.
old-location: base\interlockedbittestandset.htm
tech.root: Sync
ms.assetid: 26c1f4b5-02db-4316-ab5d-23e60fc6b116
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: InterlockedBitTestAndSet, InterlockedBitTestAndSet function, _interlockedbittestandset, base.interlockedbittestandset, winnt/InterlockedBitTestAndSet
ms.topic: function
req.header: winnt.h
req.include-header: Windows.h
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
 - Winnt.h
api_name:
 - InterlockedBitTestAndSet
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# _interlockedbittestandset function


## -description


Tests the specified bit of the specified <b>LONG</b> value and sets it to 1. The operation is atomic.


## -parameters




### -param Base [in]

A pointer to a variable.


### -param Offset [in]

The bit position to be tested.


## -returns



The value of the specified bit.




## -remarks



The interlocked functions provide a simple mechanism for synchronizing access to a variable that is shared by multiple threads. This function is atomic with respect to calls to other interlocked functions.

This function is implemented using a compiler intrinsic where possible. For more information, see the WinBase.h header file and <a href="https://msdn.microsoft.com/library/646k06sz(v=VS.85).aspx">_interlockedbittestandset</a>.

This function  generates a full memory barrier (or fence) to ensure that memory operations are completed in order.

<div class="alert"><b>Note</b>  This function is supported on Windows RT-based systems.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/729c0e68-ef52-4d6c-b771-a89043a937e6">Interlocked Variable Access</a>



<a href="https://msdn.microsoft.com/620bc56b-e85a-403f-94b8-14c838f046f0">InterlockedBitTestAndReset</a>



<a href="https://msdn.microsoft.com/a0f05333-d391-4596-b4f1-3146b46a6108">InterlockedBitTestAndReset64</a>



<a href="https://msdn.microsoft.com/ed06cbec-23df-411d-a0c7-5b4c3511bb0a">InterlockedBitTestAndResetAcquire</a>



<a href="https://msdn.microsoft.com/75261ed0-5322-4560-b7d2-447f6f7e0c8a">InterlockedBitTestAndResetRelease</a>



<a href="https://msdn.microsoft.com/27f344c7-7143-42fe-b5b6-adc1d983abde">InterlockedBitTestAndSet64</a>



<a href="https://msdn.microsoft.com/3ae1ae36-eb50-4fe5-af7c-6366af7fd73a">InterlockedBitTestAndSetAcquire</a>



<a href="https://msdn.microsoft.com/f577867e-66b0-4e0b-ac5b-5a554d3e33f0">InterlockedBitTestAndSetRelease</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>
 

 

