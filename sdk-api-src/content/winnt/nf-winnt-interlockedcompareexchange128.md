---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# InterlockedCompareExchange128 function


## -description


Performs an atomic compare-and-exchange operation on the specified values. The function compares two specified 128-bit values and exchanges with another 128-bit value based on the outcome of the comparison.

To operate on 16-bit values, use the <a href="https://msdn.microsoft.com/5bf2e0d7-1b64-4622-8b6f-4ac903027064">InterlockedCompareExchange16</a> function.

To operate on 32-bit values, use the <a href="https://msdn.microsoft.com/library/windows/hardware/ff547853">InterlockedCompareExchange</a> function.

To operate on 64-bit values, use the <a href="https://msdn.microsoft.com/b0799de3-49f9-4eef-9c14-d145f42ce57b">InterlockedCompareExchange64</a> function.


## -parameters




### -param Destination [in, out]

 A pointer to the destination value.  This parameter is an array of two 64-bit integers considered as a 128-bit field. 


### -param ExchangeHigh [in]

The high part of the exchange value.


### -param ExchangeLow [in]

The low part of the exchange value.


### -param ComparandResult [in, out]

The value to compare to. This parameter is an array of two 64-bit integers considered as a 128-bit field. On output, this is overwritten with the original value of the destination.


## -returns



The function returns 1 if <i>ComparandResult</i> equals the original value of the <i>Destination</i> parameter, or 0 if <i>ComparandResult</i> does not equal the original value of the <i>Destination</i> parameter.




## -remarks



The 
function compares the <i>Destination</i> value with the <i>ComparandResult</i> value:

<ul>
<li>If the <i>Destination</i> value is equal to the <i>ComparandResult</i> value, the <i>ExchangeHigh</i> and <i>ExchangeLow</i> values are stored in the array specified by <i>Destination</i>, and also in the array specified by <i>ComparandResult</i>.</li>
<li>Otherwise, the <i>Destination</i> is left unmodified. </li>
</ul>
Regardless of the result of the comparison, the original <i>Destination</i> value is stored in the array specified by <i>ComparandResult</i>.

The parameters for this function must be aligned on a 16-byte boundary; otherwise, the function will behave unpredictably on x64 systems. See <b>_aligned_malloc</b>.

The interlocked functions provide a simple mechanism for synchronizing access to a variable that is shared by multiple threads. This function is atomic with respect to calls to other interlocked functions.

This function is only available on x64-based systems, and it is implemented using a compiler intrinsic. For more information, see the WinBase.h header file and <a href="c3ad79c0-a523-4930-a3a4-69a65d7d5c81">_InterlockedCompareExchange128</a>.

This function generates a full memory barrier (or fence) to ensure that memory operations are completed in order.




## -see-also




<a href="https://msdn.microsoft.com/729c0e68-ef52-4d6c-b771-a89043a937e6">Interlocked Variable Access</a>



<a href="https://msdn.microsoft.com/8bd9dfe3-2d98-46a0-9212-5e3d9d7a2ac1">InterlockedCompare64Exchange128</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff547853">InterlockedCompareExchange</a>



<a href="https://msdn.microsoft.com/5bf2e0d7-1b64-4622-8b6f-4ac903027064">InterlockedCompareExchange16</a>



<a href="https://msdn.microsoft.com/d9b24d63-0544-41e3-ad4e-d90cd9bd6a03">InterlockedCompareExchange16Acquire</a>



<a href="https://msdn.microsoft.com/6c53a500-f5a7-45ce-921d-efa1059327b6">InterlockedCompareExchange16NoFence</a>



<a href="https://msdn.microsoft.com/d8c69974-2828-42b8-878d-621ec696e950">InterlockedCompareExchange16Release</a>



<a href="https://msdn.microsoft.com/b0799de3-49f9-4eef-9c14-d145f42ce57b">InterlockedCompareExchange64</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff547857">InterlockedCompareExchangeAcquire</a>



<a href="https://msdn.microsoft.com/15a88896-3a45-4f81-b62c-99d5f904162b">InterlockedCompareExchangeAcquire64</a>



<a href="https://msdn.microsoft.com/2637d8a7-b0f7-467e-9939-e8a3336970f2">InterlockedCompareExchangeNoFence</a>



<a href="https://msdn.microsoft.com/c8794b4c-2b81-4636-ac70-d9ea9f287783">InterlockedCompareExchangeNoFence64</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff547863">InterlockedCompareExchangePointer</a>



<a href="https://msdn.microsoft.com/dc57e723-3eaa-42a2-b0a6-6b55a34e77ba">InterlockedCompareExchangePointerAcquire</a>



<a href="https://msdn.microsoft.com/f2004070-ae5d-4cfb-94ad-90490f495f5b">InterlockedCompareExchangePointerNoFence</a>



<a href="https://msdn.microsoft.com/d2552edc-1efe-4148-890f-0e7fe71a7313">InterlockedCompareExchangePointerRelease</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff547867">InterlockedCompareExchangeRelease</a>



<a href="https://msdn.microsoft.com/833b0e9d-e8c8-40dd-9907-5a5f92bf6bac">InterlockedCompareExchangeRelease64</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>
 

 

