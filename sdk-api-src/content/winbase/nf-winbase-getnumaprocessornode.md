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

# GetNumaProcessorNode function


## -description


Retrieves the node number for the specified processor.

Use the <a href="https://msdn.microsoft.com/6b843cd8-eeb5-4aa1-aad4-ce98916346b1">GetNumaProcessorNodeEx</a> function to specify a processor group and retrieve the node number as a <b>USHORT</b> value.


## -parameters




### -param Processor [in]

The processor number.

On a system with more than 64 logical processors, the processor number is relative to the <a href="https://msdn.microsoft.com/c627ac0f-96e8-48b5-9103-4316f487e173">processor group</a> that contains the processor on which the calling thread is running.


### -param NodeNumber [out]

The node number. If the processor does not exist, this parameter is 0xFF.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To retrieve the list of processors on the system, use the 
<a href="https://msdn.microsoft.com/f50ca86e-fa81-4ed9-ae6c-63a4e7f2a53f">GetProcessAffinityMask</a> function.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/df025b35-fb6b-4987-806e-9c76e6b130a1">Allocating Memory from a NUMA Node</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/bdaecb36-9b51-4cc3-88b3-0dbd63bdc9b8">GetNumaNodeProcessorMask</a>



<a href="https://msdn.microsoft.com/6b843cd8-eeb5-4aa1-aad4-ce98916346b1">GetNumaProcessorNodeEx</a>



<a href="https://msdn.microsoft.com/9a2dbfe3-13e7-442d-a5f6-b2632878f618">GetNumaProximityNode</a>



<a href="https://msdn.microsoft.com/f50ca86e-fa81-4ed9-ae6c-63a4e7f2a53f">GetProcessAffinityMask</a>



<a href="https://msdn.microsoft.com/a1263968-2b26-45cc-bdd7-6aa354821a5a">NUMA Support</a>
 

 

