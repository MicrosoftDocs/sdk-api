---
UID: NF:winnt.InterlockedAnd8
title: InterlockedAnd8 function
author: windows-sdk-content
description: Performs an atomic AND operation on the specified char values.
old-location: base\interlockedand8.htm
tech.root: sync
ms.assetid: 1b900308-f1dd-465b-b67d-ec2655819425
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: InterlockedAnd8, InterlockedAnd8 function, base.interlockedand8, winnt/InterlockedAnd8
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - InterlockedAnd8
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# InterlockedAnd8 function


## -description


Performs an atomic AND operation on the specified <b>char</b> values.


## -parameters




### -param Destination [in, out]

A pointer to the first operand. This value will be replaced with the result of the operation.


### -param Value [in]

The second operand.


## -returns



The function returns the original value of the <i>Destination</i> parameter.




## -remarks



The interlocked functions provide a simple mechanism for synchronizing access to a variable that is shared by multiple threads. This function is atomic with respect to calls to other interlocked functions.

For the Intel Itanium-based systems and x64 architectures, this function is implemented using the compiler intrinsic. For the x86 architecture, use the <a href="ad271dc3-42cd-47d0-9f65-30d5cfeb66fc">_InterlockedAnd8</a> compiler intrinsic directly.

This function  generates a full memory barrier (or fence) to ensure that memory operations are completed in order.

<b>Itanium-based systems:  </b>For performance-critical applications, use <a href="https://msdn.microsoft.com/b4f9e33b-e770-4033-a216-3eab79262909">InterlockedAnd8Acquire</a> or <a href="https://msdn.microsoft.com/10d400dd-f353-484c-ad97-048c85e3a862">InterlockedAnd8Release</a> instead.

<div class="alert"><b>Note</b>  This function is supported on Windows RT-based systems.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/729c0e68-ef52-4d6c-b771-a89043a937e6">Interlocked Variable Access</a>



<a href="https://msdn.microsoft.com/463b579e-d1cd-4ad5-b2f2-bae599849401">InterlockedAnd</a>



<a href="https://msdn.microsoft.com/2fadfee3-929e-4087-a1c9-789a881c7a25">InterlockedAnd16</a>



<a href="https://msdn.microsoft.com/1370d3dc-bac9-46e0-8152-f43f082721f0">InterlockedAnd16Acquire</a>



<a href="https://msdn.microsoft.com/b5965bb4-b2da-4b5b-9398-3f6024bb11ac">InterlockedAnd16NoFence</a>



<a href="https://msdn.microsoft.com/ef68c1a8-9a7c-445f-95b2-c8cf95f46a8c">InterlockedAnd16Release</a>



<a href="https://msdn.microsoft.com/544b0710-3394-4123-88e1-0621de5fe7b6">InterlockedAnd64</a>



<a href="https://msdn.microsoft.com/854e0666-13d5-4268-be82-346a715beff1">InterlockedAnd64Acquire</a>



<a href="https://msdn.microsoft.com/9634aa22-674a-4bbe-a3ef-3c29a382149e">InterlockedAnd64NoFence</a>



<a href="https://msdn.microsoft.com/1f8d4b23-aa14-45bc-ae99-65ade516cd95">InterlockedAnd64Release</a>



<a href="https://msdn.microsoft.com/b4f9e33b-e770-4033-a216-3eab79262909">InterlockedAnd8Acquire</a>



<a href="https://msdn.microsoft.com/a534e4aa-a895-41fa-a71f-b89f4769dbc2">InterlockedAnd8NoFence</a>



<a href="https://msdn.microsoft.com/10d400dd-f353-484c-ad97-048c85e3a862">InterlockedAnd8Release</a>



<a href="https://msdn.microsoft.com/d060b199-78c8-497c-8ed9-ac86f03f17f2">InterlockedAndAcquire</a>



<a href="https://msdn.microsoft.com/bb5312f8-ec57-4b75-9443-dd33a2e5c080">InterlockedAndNoFence</a>



<a href="https://msdn.microsoft.com/a651293e-f4d7-466d-870f-ccfba2b977c3">InterlockedAndRelease</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>
 

 

