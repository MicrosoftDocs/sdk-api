---
UID: NF:winbase.GetNumaNodeProcessorMask
title: GetNumaNodeProcessorMask function
author: windows-sdk-content
description: Retrieves the processor mask for the specified node.
old-location: base\getnumanodeprocessormask.htm
tech.root: procthread
ms.assetid: bdaecb36-9b51-4cc3-88b3-0dbd63bdc9b8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetNumaNodeProcessorMask, GetNumaNodeProcessorMask function, _win32_getnumanodeprocessormask, base.getnumanodeprocessormask, winbase/GetNumaNodeProcessorMask
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - Kernel32Legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - GetNumaNodeProcessorMask
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetNumaNodeProcessorMask function


## -description


Retrieves the processor mask for the specified node. 

Use the <a href="https://msdn.microsoft.com/4baf7193-aab3-4bd0-bc0a-60fd9277fc72">GetNumaNodeProcessorMaskEx</a> function to retrieve the processor mask for a node in any processor group.


## -parameters




### -param Node [in]

The number of the node.


### -param ProcessorMask [out]

The processor mask for the node. A processor mask is a bit vector in which each bit represents a processor and whether it is in the node.

If the node has no processors configured, the processor mask is zero.

On systems with more than 64 processors, this parameter is set to the processor mask for the node only if the node is in the same <a href="https://msdn.microsoft.com/c627ac0f-96e8-48b5-9103-4316f487e173">processor group</a> as the calling thread. Otherwise, the parameter is set to zero.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To retrieve the highest numbered node in the system, use the 
<a href="https://msdn.microsoft.com/ce944fa7-b42a-4b99-ac8d-30bd026fba21">GetNumaHighestNodeNumber</a> function. Note that this number is not guaranteed to equal the total number of nodes in the system.

To ensure that all threads for your process run on the same node, use the 
<a href="https://msdn.microsoft.com/210b4c95-4072-4039-aa4f-6b0d85758359">SetProcessAffinityMask</a> function with a process affinity mask that specifies processors in the same node.




## -see-also




<a href="https://msdn.microsoft.com/4baf7193-aab3-4bd0-bc0a-60fd9277fc72">GetNumaNodeProcessorMaskEx</a>



<a href="https://msdn.microsoft.com/88e6c6b3-7ec5-43e5-8cf3-21402925f718">GetNumaProcessorNode</a>



<a href="https://msdn.microsoft.com/a1263968-2b26-45cc-bdd7-6aa354821a5a">NUMA Support</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/210b4c95-4072-4039-aa4f-6b0d85758359">SetProcessAffinityMask</a>
 

 

