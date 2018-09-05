---
UID: NF:winnt._InlineInterlockedAdd64
title: "_InlineInterlockedAdd64 function"
author: windows-sdk-content
description: Performs an atomic addition operation on the specified LONGLONG values.
old-location: base\interlockedadd64.htm
old-project: Sync
ms.assetid: ab37292f-4291-4cca-826c-d6488e141db8
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: InterlockedAdd64, InterlockedAdd64 function, _InlineInterlockedAdd64, base.interlockedadd64, winnt/InterlockedAdd64
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winnt.h
req.include-header: Windows.h
req.redist: 
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
 - InterlockedAdd64
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _InlineInterlockedAdd64 function


## -description


Performs an atomic addition operation on the specified <b>LONGLONG</b> values.


## -parameters




### -param Addend [in, out]

A pointer to the first operand. This value will be replaced with the result of the operation.


### -param Value [in]

The second operand.


## -returns



The function returns the result of the operation.




## -remarks



The interlocked functions provide a simple mechanism for synchronizing access to a variable that is shared by multiple threads. This function is atomic with respect to calls to other interlocked functions.

This function is implemented using a compiler intrinsic where possible. For more information, see the WinBase.h header file and <a href="3d319603-ea9c-4fdd-ae61-e52430ccc3b1">_InterlockedAdd64</a>.

This function  generates a full memory barrier (or fence) to ensure that memory operations are completed in order.

<div class="alert"><b>Note</b>  This function is supported on Windows RT-based systems.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/729c0e68-ef52-4d6c-b771-a89043a937e6">Interlocked Variable Access</a>



<a href="https://msdn.microsoft.com/c3ff4c2f-ac84-4046-ac4e-600569b874be">InterlockedAdd</a>



<a href="https://msdn.microsoft.com/ec1746cc-aff9-440e-b7e1-15a3d7a0fa58">InterlockedAddAcquire</a>



<a href="https://msdn.microsoft.com/0bdce93f-a57a-40d3-a8fa-007edb8b5c6d">InterlockedAddAcquire64</a>



<a href="https://msdn.microsoft.com/98f29a64-27c9-455f-a7cf-c2c47ea512c8">InterlockedAddNoFence</a>



<a href="https://msdn.microsoft.com/f7c8c50a-805f-4963-8a5e-160776dd995e">InterlockedAddNoFence64</a>



<a href="https://msdn.microsoft.com/d09a6420-bf6c-43a7-aa7a-1cff03596afc">InterlockedAddRelease</a>



<a href="https://msdn.microsoft.com/24a88190-79e3-48bf-986e-d5d08c1bce08">InterlockedAddRelease64</a>



<a href="https://msdn.microsoft.com/e48b67a0-133b-4e88-b451-432f26b4881a">InterlockedExchangeAdd</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>
 

 

