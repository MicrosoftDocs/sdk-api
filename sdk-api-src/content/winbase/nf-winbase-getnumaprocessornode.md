---
UID: NF:winbase.GetNumaProcessorNode
title: GetNumaProcessorNode function
author: windows-driver-content
description: Retrieves the node number for the specified processor.
old-location: base\getnumaprocessornode.htm
old-project: ProcThread
ms.assetid: 88e6c6b3-7ec5-43e5-8cf3-21402925f718
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: GetNumaProcessorNode, GetNumaProcessorNode function, _win32_getnumaprocessornode, base.getnumaprocessornode, winbase/GetNumaProcessorNode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP Professional x64 Edition, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PRIORITY_HINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
api_name:
-	GetNumaProcessorNode
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
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
 

 

