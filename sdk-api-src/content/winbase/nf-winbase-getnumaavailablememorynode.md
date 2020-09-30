---
UID: NF:winbase.GetNumaAvailableMemoryNode
title: GetNumaAvailableMemoryNode function (winbase.h)
description: Retrieves the amount of memory available in the specified node.
helpviewer_keywords: ["GetNumaAvailableMemoryNode","GetNumaAvailableMemoryNode function","_win32_getnumaavailablememorynode","base.getnumaavailablememorynode","winbase/GetNumaAvailableMemoryNode"]
old-location: base\getnumaavailablememorynode.htm
tech.root: backup
ms.assetid: 8db45ec1-fa3c-4395-8986-817e8b137a8a
ms.date: 12/05/2018
ms.keywords: GetNumaAvailableMemoryNode, GetNumaAvailableMemoryNode function, _win32_getnumaavailablememorynode, base.getnumaavailablememorynode, winbase/GetNumaAvailableMemoryNode
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
 - GetNumaAvailableMemoryNode
 - winbase/GetNumaAvailableMemoryNode
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
 - GetNumaAvailableMemoryNode
---

# GetNumaAvailableMemoryNode function


## -description

Retrieves the amount of memory available in the specified node. 

Use the <a href="/windows/desktop/api/winbase/nf-winbase-getnumaavailablememorynodeex">GetNumaAvailableMemoryNodeEx</a> function to specify the node  as a <b>USHORT</b> value.

## -parameters

### -param Node [in]

The number of the node.

### -param AvailableBytes [out]

The amount of available memory for the node, in bytes.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>GetNumaAvailableMemoryNode</b> function returns the amount of memory consumed by free and zeroed pages on the specified node. On systems with more than one node, this memory does not include standby pages. Therefore, the sum of the available memory values for all nodes in the system is equal to the value of the Free &amp; Zero Page List Bytes memory performance counter. On systems with only one node, the value returned by <b>GetNumaAvailableMemoryNode</b>  includes standby pages and  is equal to the value of the Available Bytes memory performance counter. For more information about performance counters, see <a href="/previous-versions/windows/desktop/legacy/aa965225(v=vs.85)">Memory Performance Information</a>.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-getnumaavailablememorynodeex">GetNumaAvailableMemoryNodeEx</a>



<a href="/windows/desktop/ProcThread/numa-support">NUMA Support</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>