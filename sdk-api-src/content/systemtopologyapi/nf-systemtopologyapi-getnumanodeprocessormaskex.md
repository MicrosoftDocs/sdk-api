---
UID: NF:systemtopologyapi.GetNumaNodeProcessorMaskEx
title: GetNumaNodeProcessorMaskEx function (systemtopologyapi.h)
author: windows-sdk-content
description: Retrieves the processor mask for a node regardless of the processor group the node belongs to.
old-location: base\getnumanodeprocessormaskex.htm
tech.root: ProcThread
ms.assetid: 4baf7193-aab3-4bd0-bc0a-60fd9277fc72
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetNumaNodeProcessorMaskEx, GetNumaNodeProcessorMaskEx function, base.getnumanodeprocessormaskex, systemtopologyapi/GetNumaNodeProcessorMaskEx, winbase/GetNumaNodeProcessorMaskEx
ms.topic: function
req.header: systemtopologyapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - kernel32.dll
 - API-MS-Win-Core-systemtopology-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - API-MS-Win-Core-Systemtopology-L1-1-1.dll
api_name:
 - GetNumaNodeProcessorMaskEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetNumaNodeProcessorMaskEx function


## -description


Retrieves the processor mask for a node regardless of the processor group the node belongs to.


## -parameters




### -param Node [in]

The node number.


### -param ProcessorMask [out]

A pointer to a <a href="https://msdn.microsoft.com/76009431-9139-4c03-9c7b-0c4bb5f0cb83">GROUP_AFFINITY</a> structure that receives the processor mask for the specified node. A processor mask is a bit vector in which each bit represents a processor and whether it is in the node.

If the specified node has no processors configured, the <b>Mask</b> member is zero and the <b>Group</b> member is undefined.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The <b>GetNumaNodeProcessorMaskEx</b> function differs from <a href="https://msdn.microsoft.com/bdaecb36-9b51-4cc3-88b3-0dbd63bdc9b8">GetNumaNodeProcessorMask</a> in that it can retrieve the processor mask for a node regardless of the group the node belongs to. That is, the node does not have to be in the same group as the calling thread. The <b>GetNumaNodeProcessorMask</b> function can retrieve the processor mask only for nodes that are in the same group as the calling thread.

To retrieve the highest numbered node in the system, use the 
<a href="https://msdn.microsoft.com/ce944fa7-b42a-4b99-ac8d-30bd026fba21">GetNumaHighestNodeNumber</a> function. Note that this number is not guaranteed to equal the total number of nodes in the system.

To ensure that all threads for your process run on the same node, use the 
<a href="https://msdn.microsoft.com/210b4c95-4072-4039-aa4f-6b0d85758359">SetProcessAffinityMask</a> function with a process affinity mask that specifies processors in the same node.

To compile an application that uses this function, set <b>_WIN32_WINNT</b> &gt;= 0x0601. For more information, see <a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/76009431-9139-4c03-9c7b-0c4bb5f0cb83">GROUP_AFFINITY</a>



<a href="https://msdn.microsoft.com/bdaecb36-9b51-4cc3-88b3-0dbd63bdc9b8">GetNumaNodeProcessorMask</a>



<a href="https://msdn.microsoft.com/a1263968-2b26-45cc-bdd7-6aa354821a5a">NUMA Support</a>



<a href="https://msdn.microsoft.com/c627ac0f-96e8-48b5-9103-4316f487e173">Processor Groups</a>
 

 

