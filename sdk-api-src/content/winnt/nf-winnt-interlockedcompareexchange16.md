---
UID: NF:winnt.InterlockedCompareExchange16
title: InterlockedCompareExchange16 function
author: windows-sdk-content
description: Performs an atomic compare-and-exchange operation on the specified values. The function compares two specified 16-bit values and exchanges with another 16-bit value based on the outcome of the comparison.
old-location: base\interlockedcompareexchange16.htm
tech.root: Sync
ms.assetid: 5bf2e0d7-1b64-4622-8b6f-4ac903027064
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: InterlockedCompareExchange16, InterlockedCompareExchange16 function, base.interlockedcompareexchange16, winnt/InterlockedCompareExchange16
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - InterlockedCompareExchange16
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# InterlockedCompareExchange16 function


## -description


Performs an atomic compare-and-exchange operation on the specified values. The function compares two specified 16-bit values and exchanges with another 16-bit value based on the outcome of the comparison.

To operate on 32-bit values, use the <a href="https://msdn.microsoft.com/c0da780c-5fd0-4c88-a283-8d057db812ac">InterlockedCompareExchange</a> function.

To operate on 64-bit values, use the <a href="https://msdn.microsoft.com/b0799de3-49f9-4eef-9c14-d145f42ce57b">InterlockedCompareExchange64</a> function.

To operate on 128-bit values, use the <a href="https://msdn.microsoft.com/55a5ec1d-9c81-479e-a630-81756bf620d1">InterlockedCompareExchange128</a> function.


## -parameters




### -param Destination [in, out]

 A pointer to the destination value.


### -param ExChange [in]

The exchange value.


### -param Comperand [in]

The value to compare to <i>Destination</i>.


## -returns



The function returns the initial value of the <i>Destination</i> parameter.




## -remarks



The 
function compares the <i>Destination</i> value with the <i>Comparand</i> value. If the <i>Destination</i> value is equal to the <i>Comparand</i> value, the <i>Exchange</i> value is stored in the address specified by <i>Destination</i>. Otherwise, no operation is performed.

The parameters for this function must be aligned on a 16-bit boundary; otherwise, the function will behave unpredictably on multiprocessor x86 systems and any non-x86 systems. See <b>_aligned_malloc</b>.

The interlocked functions provide a simple mechanism for synchronizing access to a variable that is shared by multiple threads. This function is atomic with respect to calls to other interlocked functions.

This function is implemented using a compiler intrinsic where possible. For more information, see the WinBase.h header file and <a href="c3ad79c0-a523-4930-a3a4-69a65d7d5c81">_InterlockedCompareExchange16</a>.

This function generates a full memory barrier (or fence) to ensure that memory operations are completed in order.

<div class="alert"><b>Note</b>  This function is supported on Windows RT-based systems.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/729c0e68-ef52-4d6c-b771-a89043a937e6">Interlocked Variable Access</a>



<a href="https://msdn.microsoft.com/8bd9dfe3-2d98-46a0-9212-5e3d9d7a2ac1">InterlockedCompare64Exchange128</a>



<a href="https://msdn.microsoft.com/c0da780c-5fd0-4c88-a283-8d057db812ac">InterlockedCompareExchange</a>



<a href="https://msdn.microsoft.com/55a5ec1d-9c81-479e-a630-81756bf620d1">InterlockedCompareExchange128</a>



<a href="https://msdn.microsoft.com/d9b24d63-0544-41e3-ad4e-d90cd9bd6a03">InterlockedCompareExchange16Acquire</a>



<a href="https://msdn.microsoft.com/6c53a500-f5a7-45ce-921d-efa1059327b6">InterlockedCompareExchange16NoFence</a>



<a href="https://msdn.microsoft.com/d8c69974-2828-42b8-878d-621ec696e950">InterlockedCompareExchange16Release</a>



<a href="https://msdn.microsoft.com/b0799de3-49f9-4eef-9c14-d145f42ce57b">InterlockedCompareExchange64</a>



<a href="https://msdn.microsoft.com/6cb7d17b-dfda-431e-9c74-cc42d62202ba">InterlockedCompareExchangeAcquire</a>



<a href="https://msdn.microsoft.com/15a88896-3a45-4f81-b62c-99d5f904162b">InterlockedCompareExchangeAcquire64</a>



<a href="https://msdn.microsoft.com/2637d8a7-b0f7-467e-9939-e8a3336970f2">InterlockedCompareExchangeNoFence</a>



<a href="https://msdn.microsoft.com/c8794b4c-2b81-4636-ac70-d9ea9f287783">InterlockedCompareExchangeNoFence64</a>



<a href="https://msdn.microsoft.com/15c1fadd-9e0d-4254-ae14-82b0ce46909e">InterlockedCompareExchangePointer</a>



<a href="https://msdn.microsoft.com/dc57e723-3eaa-42a2-b0a6-6b55a34e77ba">InterlockedCompareExchangePointerAcquire</a>



<a href="https://msdn.microsoft.com/f2004070-ae5d-4cfb-94ad-90490f495f5b">InterlockedCompareExchangePointerNoFence</a>



<a href="https://msdn.microsoft.com/d2552edc-1efe-4148-890f-0e7fe71a7313">InterlockedCompareExchangePointerRelease</a>



<a href="https://msdn.microsoft.com/3e35f752-dc58-4a87-8284-bdbe5692aaa6">InterlockedCompareExchangeRelease</a>



<a href="https://msdn.microsoft.com/833b0e9d-e8c8-40dd-9907-5a5f92bf6bac">InterlockedCompareExchangeRelease64</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>
 

 

