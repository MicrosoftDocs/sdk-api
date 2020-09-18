---
UID: NF:winbase.GetNumaProcessorNode
title: GetNumaProcessorNode function (winbase.h)
description: Retrieves the node number for the specified processor.
helpviewer_keywords: ["GetNumaProcessorNode","GetNumaProcessorNode function","_win32_getnumaprocessornode","base.getnumaprocessornode","winbase/GetNumaProcessorNode"]
old-location: base\getnumaprocessornode.htm
tech.root: backup
ms.assetid: 88e6c6b3-7ec5-43e5-8cf3-21402925f718
ms.date: 12/05/2018
ms.keywords: GetNumaProcessorNode, GetNumaProcessorNode function, _win32_getnumaprocessornode, base.getnumaprocessornode, winbase/GetNumaProcessorNode
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
 - GetNumaProcessorNode
 - winbase/GetNumaProcessorNode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - GetNumaProcessorNode
---

# GetNumaProcessorNode function


## -description

Retrieves the node number for the specified processor.

Use the <a href="/windows/desktop/api/winbase/nf-winbase-getnumaprocessornodeex">GetNumaProcessorNodeEx</a> function to specify a processor group and retrieve the node number as a <b>USHORT</b> value.

## -parameters

### -param Processor [in]

The processor number.

On a system with more than 64 logical processors, the processor number is relative to the <a href="/windows/desktop/ProcThread/processor-groups">processor group</a> that contains the processor on which the calling thread is running.

### -param NodeNumber [out]

The node number. If the processor does not exist, this parameter is 0xFF.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

To retrieve the list of processors on the system, use the 
<a href="/windows/desktop/api/winbase/nf-winbase-getprocessaffinitymask">GetProcessAffinityMask</a> function.


#### Examples

For an example, see <a href="/windows/desktop/Memory/allocating-memory-from-a-numa-node">Allocating Memory from a NUMA Node</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-getnumanodeprocessormask">GetNumaNodeProcessorMask</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getnumaprocessornodeex">GetNumaProcessorNodeEx</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getnumaproximitynode">GetNumaProximityNode</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getprocessaffinitymask">GetProcessAffinityMask</a>



<a href="/windows/desktop/ProcThread/numa-support">NUMA Support</a>