---
UID: NF:winbase.GetNumaNodeProcessorMask
title: GetNumaNodeProcessorMask function (winbase.h)
description: Retrieves the processor mask for the specified node.
helpviewer_keywords: ["GetNumaNodeProcessorMask","GetNumaNodeProcessorMask function","_win32_getnumanodeprocessormask","base.getnumanodeprocessormask","winbase/GetNumaNodeProcessorMask"]
old-location: base\getnumanodeprocessormask.htm
tech.root: backup
ms.assetid: bdaecb36-9b51-4cc3-88b3-0dbd63bdc9b8
ms.date: 03/15/2021
ms.keywords: GetNumaNodeProcessorMask, GetNumaNodeProcessorMask function, _win32_getnumanodeprocessormask, base.getnumanodeprocessormask, winbase/GetNumaNodeProcessorMask
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetNumaNodeProcessorMask
 - winbase/GetNumaNodeProcessorMask
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-kernel32-legacy-l1-1-6.dll
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - Kernel32Legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - GetNumaNodeProcessorMask
---

# GetNumaNodeProcessorMask function


## -description

Retrieves the processor mask for the specified node. 

## -parameters

### -param Node [in]

The number of the node.

### -param ProcessorMask [out]

The processor mask for the node. A processor mask is a bit vector in which each bit represents a processor and whether it is in the node.

If the node has no processors configured, the processor mask is zero.

On systems with more than 64 processors, this parameter is set to the processor mask for the node only if the node is in the same <a href="/windows/desktop/ProcThread/processor-groups">processor group</a> as the calling thread. Otherwise, the parameter is set to zero.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

To retrieve the highest numbered node in the system, use the 
<a href="/windows/desktop/api/systemtopologyapi/nf-systemtopologyapi-getnumahighestnodenumber">GetNumaHighestNodeNumber</a> function. Note that this number is not guaranteed to equal the total number of nodes in the system.

To ensure that all threads for your process run on the same node, use the 
<a href="/windows/desktop/api/winbase/nf-winbase-setprocessaffinitymask">SetProcessAffinityMask</a> function with a process affinity mask that specifies processors in the same node.

Use the <a href="/windows/desktop/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormaskex">GetNumaNodeProcessorMaskEx</a> function to retrieve the processor mask for a node in any processor group.

> [!NOTE]
> Starting with *TBD Release Iron*, the behavior of this and other NUMA functions has been modified to better support systems with nodes containing more that 64 processors. For more information about this change, including information about enabling the old behavior of this API, see [NUMA Support](/windows/win32/procthread/numa-support).

### Behavior starting with TBD Release Iron

Each node is assigned a primary group by the system. The mask returned by **GetNumaNodeProcessorMask** is for the node's primary group and is only returned if the calling thread belongs to that group.

### Behavior in previous versions

The mask for the specified node is returned.

## -see-also

<a href="/windows/desktop/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormaskex">GetNumaNodeProcessorMaskEx</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getnumaprocessornode">GetNumaProcessorNode</a>



<a href="/windows/desktop/ProcThread/numa-support">NUMA Support</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setprocessaffinitymask">SetProcessAffinityMask</a>