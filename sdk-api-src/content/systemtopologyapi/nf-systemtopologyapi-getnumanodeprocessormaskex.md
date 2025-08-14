---
UID: NF:systemtopologyapi.GetNumaNodeProcessorMaskEx
title: GetNumaNodeProcessorMaskEx function (systemtopologyapi.h)
description: Retrieves the processor mask for a node regardless of the processor group the node belongs to.
helpviewer_keywords: ["GetNumaNodeProcessorMaskEx","GetNumaNodeProcessorMaskEx function","base.getnumanodeprocessormaskex","systemtopologyapi/GetNumaNodeProcessorMaskEx","winbase/GetNumaNodeProcessorMaskEx"]
old-location: base\getnumanodeprocessormaskex.htm
tech.root: ProcThread
ms.assetid: 4baf7193-aab3-4bd0-bc0a-60fd9277fc72
ms.date: 03/15/2021
ms.keywords: GetNumaNodeProcessorMaskEx, GetNumaNodeProcessorMaskEx function, base.getnumanodeprocessormaskex, systemtopologyapi/GetNumaNodeProcessorMaskEx, winbase/GetNumaNodeProcessorMaskEx
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetNumaNodeProcessorMaskEx
 - systemtopologyapi/GetNumaNodeProcessorMaskEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-systemtopology-l1-1-2.dll
 - kernel32.dll
 - API-MS-Win-Core-systemtopology-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - API-MS-Win-Core-Systemtopology-L1-1-1.dll
api_name:
 - GetNumaNodeProcessorMaskEx
---

# GetNumaNodeProcessorMaskEx function


## -description

Retrieves the processor mask for a node regardless of the processor group the node belongs to.

## -parameters

### -param Node [in]

The node number.

### -param ProcessorMask [out]

A pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-group_affinity">GROUP_AFFINITY</a> structure that receives the processor mask for the specified node. A processor mask is a bit vector in which each bit represents a processor and whether it is in the node.

If the specified node has no processors configured, the <b>Mask</b> member is zero and the <b>Group</b> member is undefined.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The <b>GetNumaNodeProcessorMaskEx</b> function differs from <a href="/windows/desktop/api/winbase/nf-winbase-getnumanodeprocessormask">GetNumaNodeProcessorMask</a> in that it can retrieve the processor mask for a node regardless of the group the node belongs to. That is, the node does not have to be in the same group as the calling thread. The <b>GetNumaNodeProcessorMask</b> function can retrieve the processor mask only for nodes that are in the same group as the calling thread.

To retrieve the highest numbered node in the system, use the 
<a href="/windows/desktop/api/systemtopologyapi/nf-systemtopologyapi-getnumahighestnodenumber">GetNumaHighestNodeNumber</a> function. Note that this number is not guaranteed to equal the total number of nodes in the system.

To ensure that all threads for your process run on the same node, use the 
<a href="/windows/desktop/api/winbase/nf-winbase-setprocessaffinitymask">SetProcessAffinityMask</a> function with a process affinity mask that specifies processors in the same node.

To compile an application that uses this function, set <b>_WIN32_WINNT</b> &gt;= 0x0601. For more information, see <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.


> [!NOTE]
> Starting with *TBD Release Iron*, the behavior of this and other NUMA functions has been modified to better support systems with nodes containing more that 64 processors. For more information about this change, including information about enabling the old behavior of this API, see [NUMA Support](/windows/win32/procthread/numa-support).

### Behavior starting with TBD Release Iron

Each node is assigned a primary group by the system. The **GROUP_AFFINITY** returned by **GetNumaNodeProcessorMaskEx** is for the node's primary group.

### Behavior in previous versions

The **GROUP_AFFINITY** for the specified node is returned.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-group_affinity">GROUP_AFFINITY</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getnumanodeprocessormask">GetNumaNodeProcessorMask</a>



<a href="/windows/desktop/ProcThread/numa-support">NUMA Support</a>



<a href="/windows/desktop/ProcThread/processor-groups">Processor Groups</a>