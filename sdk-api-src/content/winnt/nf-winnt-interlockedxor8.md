---
UID: NF:winnt.InterlockedXor8
title: InterlockedXor8 function
author: windows-sdk-content
description: Performs an atomic XOR operation on the specified char values.
old-location: base\interlockedxor8.htm
old-project: sync
ms.assetid: 9b96417e-dc2e-4b67-8084-0c0219444299
ms.author: windowssdkdev
ms.date: 08/17/2018
ms.keywords: InterlockedXor8, InterlockedXor8 function, base.interlockedxor8, winnt/InterlockedXor8
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
 - InterlockedXor8
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# InterlockedXor8 function


## -description


Performs an atomic XOR operation on the specified <b>char</b> values. The function prevents more than one thread from using the same variable simultaneously.


## -parameters




### -param Destination [in, out]

A pointer to the first operand. This value will be replaced with the result of the operation.


### -param Value [in]

The second operand.


## -returns



The function returns the original value of the <i>Destination</i> parameter.




## -remarks



The interlocked functions provide a simple mechanism for synchronizing access to a variable that is shared by multiple threads. This function is atomic with respect to calls to other interlocked functions.

For the Intel Itanium-based systems and x64 architectures, this function is implemented using the compiler intrinsic. For the x86 architecture, use the <a href="https://msdn.microsoft.com/library/a8swb4hb(v=VS.85).aspx">_InterlockedXor8</a> compiler intrinsic directly.

This function  generates a full memory barrier (or fence) to ensure that memory operations are completed in order.

<b>Itanium-based systems:  </b>For performance-critical applications, use <a href="https://msdn.microsoft.com/93194034-9794-4897-a721-0be6c20a962e">InterlockedXor8Acquire</a> or <a href="https://msdn.microsoft.com/287fd239-4a00-457d-8d40-c93047f77920">InterlockedXor8Release</a> instead.

<div class="alert"><b>Note</b>  This function is supported on Windows RT-based systems.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/729c0e68-ef52-4d6c-b771-a89043a937e6">Interlocked Variable Access</a>



<a href="https://msdn.microsoft.com/c4815bf2-e06d-4dcf-a460-a88c4c9a3c27">InterlockedXor</a>



<a href="https://msdn.microsoft.com/414830ba-ce2b-4ed0-96f4-db5edd8e4ebe">InterlockedXor16</a>



<a href="https://msdn.microsoft.com/2e3d7108-bac2-4c0e-8fad-49e81cb698b0">InterlockedXor16Acquire</a>



<a href="https://msdn.microsoft.com/615da423-6be4-40e1-a6c5-8ea7691bdad2">InterlockedXor16NoFence</a>



<a href="https://msdn.microsoft.com/f028d546-54ad-4714-9d97-0dd052b950fa">InterlockedXor16Release</a>



<a href="https://msdn.microsoft.com/b0eef2c9-5b28-462b-91cb-20a337efca7e">InterlockedXor64</a>



<a href="https://msdn.microsoft.com/f8a020ef-ec36-4e8f-b081-6c6a26227fe7">InterlockedXor64Acquire</a>



<a href="https://msdn.microsoft.com/1dbf1d34-4e10-4ae0-8ae3-f7053a941c90">InterlockedXor64NoFence</a>



<a href="https://msdn.microsoft.com/64a011a3-c920-4a68-a433-c3c216f71103">InterlockedXor64Release</a>



<a href="https://msdn.microsoft.com/93194034-9794-4897-a721-0be6c20a962e">InterlockedXor8Acquire</a>



<a href="https://msdn.microsoft.com/b58e4f02-25ca-420f-aad8-4beea9322547">InterlockedXor8NoFence</a>



<a href="https://msdn.microsoft.com/287fd239-4a00-457d-8d40-c93047f77920">InterlockedXor8Release</a>



<a href="https://msdn.microsoft.com/5a340a69-8ba2-48cb-8a7c-781a93bca826">InterlockedXorAcquire</a>



<a href="https://msdn.microsoft.com/92625f96-0548-4be2-abe9-cab2e2bb6892">InterlockedXorNoFence</a>



<a href="https://msdn.microsoft.com/55b3a88e-66da-4041-b97d-f594f11b7e04">InterlockedXorRelease</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>
 

 

