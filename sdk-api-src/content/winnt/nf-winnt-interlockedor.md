---
UID: NF:winnt.InterlockedOr
title: InterlockedOr function
author: windows-sdk-content
description: Performs an atomic OR operation on the specified LONG values.
old-location: base\interlockedor.htm
old-project: Sync
ms.assetid: c677e9fb-4188-466a-8283-9d65a50d150e
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: InterlockedOr, InterlockedOr function, base.interlockedor, winnt/InterlockedOr
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
 - InterlockedOr
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# InterlockedOr function


## -description


Performs an atomic OR operation on the specified <b>LONG</b> values. The function prevents more than one thread from using the same variable simultaneously.


## -parameters




### -param Destination [in, out]

A pointer to the first operand. This value will be replaced with the result of the operation.


### -param Value [in]

The second operand.


## -returns



The function returns the original value of the <i>Destination</i> parameter.




## -remarks



The interlocked functions provide a simple mechanism for synchronizing access to a variable that is shared by multiple threads. This function is atomic with respect to calls to other interlocked functions.

For the Intel Itanium-based systems and x64 architectures, this function is implemented using the compiler intrinsic. For the x86 architecture, use the <a href="5f265240-7af8-44b7-b952-19f3a9c56186">_InterlockedOr</a> compiler intrinsic directly.

This function  generates a full memory barrier (or fence) to ensure that memory operations are completed in order.

<b>Itanium-based systems:  </b>For performance-critical applications, use <a href="https://msdn.microsoft.com/38a2d253-cdd4-4c1e-85d9-9833f0d2a1e3">InterlockedOrAcquire</a> or <a href="https://msdn.microsoft.com/674b28f4-06ed-429f-9f2b-354fe8944962">InterlockedOrRelease</a> instead.

<div class="alert"><b>Note</b>  This function is supported on Windows RT-based systems.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/729c0e68-ef52-4d6c-b771-a89043a937e6">Interlocked Variable Access</a>



<a href="https://msdn.microsoft.com/9840313d-3c42-42ce-91b9-fde684834716">InterlockedOr16</a>



<a href="https://msdn.microsoft.com/91266b7d-43d2-46e7-a6dc-73587e232d0c">InterlockedOr16Acquire</a>



<a href="https://msdn.microsoft.com/dd3a8c9f-436a-4b95-a86b-68cc1952f73f">InterlockedOr16NoFence</a>



<a href="https://msdn.microsoft.com/f132a13b-d8ff-4092-87ed-7149880cd370">InterlockedOr16Release</a>



<a href="https://msdn.microsoft.com/ba0b03dc-de6c-4ecb-8f64-54c7c83f154a">InterlockedOr64</a>



<a href="https://msdn.microsoft.com/1e39241e-cdb0-46d4-b551-b1406afc9388">InterlockedOr64Acquire</a>



<a href="https://msdn.microsoft.com/b05c1d34-8358-488c-abb8-f215fa247ea3">InterlockedOr64NoFence</a>



<a href="https://msdn.microsoft.com/078b2794-02e1-4c83-baf9-eb3ba72edb57">InterlockedOr64Release</a>



<a href="https://msdn.microsoft.com/fa5cfecf-dde7-4d54-8dfd-68387aa86083">InterlockedOr8</a>



<a href="https://msdn.microsoft.com/d2f0fd6f-af26-4b26-a338-779df4d1772b">InterlockedOr8Acquire</a>



<a href="https://msdn.microsoft.com/d2d2f59d-e558-415a-9859-2298eec609c8">InterlockedOr8NoFence</a>



<a href="https://msdn.microsoft.com/ab09ef0d-4331-4922-8fda-0425a9116876">InterlockedOr8Release</a>



<a href="https://msdn.microsoft.com/38a2d253-cdd4-4c1e-85d9-9833f0d2a1e3">InterlockedOrAcquire</a>



<a href="https://msdn.microsoft.com/b5618ab5-1341-4606-b021-ca52a1bcf285">InterlockedOrNoFence</a>



<a href="https://msdn.microsoft.com/674b28f4-06ed-429f-9f2b-354fe8944962">InterlockedOrRelease</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>
 

 

