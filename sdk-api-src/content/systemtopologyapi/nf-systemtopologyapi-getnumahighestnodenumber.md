---
UID: NF:systemtopologyapi.GetNumaHighestNodeNumber
title: GetNumaHighestNodeNumber function (systemtopologyapi.h)
description: Retrieves the node that currently has the highest number.
helpviewer_keywords: ["GetNumaHighestNodeNumber","GetNumaHighestNodeNumber function","_win32_getnumahighestnodenumber","base.getnumahighestnodenumber","systemtopologyapi/GetNumaHighestNodeNumber","winbase/GetNumaHighestNodeNumber"]
old-location: base\getnumahighestnodenumber.htm
tech.root: ProcThread
ms.assetid: ce944fa7-b42a-4b99-ac8d-30bd026fba21
ms.date: 12/05/2018
ms.keywords: GetNumaHighestNodeNumber, GetNumaHighestNodeNumber function, _win32_getnumahighestnodenumber, base.getnumahighestnodenumber, systemtopologyapi/GetNumaHighestNodeNumber, winbase/GetNumaHighestNodeNumber
req.header: systemtopologyapi.h
req.include-header: Windows.h on Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2
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
 - GetNumaHighestNodeNumber
 - systemtopologyapi/GetNumaHighestNodeNumber
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-systemtopology-l1-1-2.dll
 - Kernel32.dll
 - API-MS-Win-Core-systemtopology-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - API-MS-Win-Core-Systemtopology-L1-1-1.dll
api_name:
 - GetNumaHighestNodeNumber
---

# GetNumaHighestNodeNumber function


## -description

Retrieves the node that currently has the highest number.

## -parameters

### -param HighestNodeNumber [out]

The number of the highest node.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The number of the highest node is not guaranteed to be the total number of nodes.

To retrieve a list of all processors in a node, use the 
<a href="/windows/desktop/api/winbase/nf-winbase-getnumanodeprocessormask">GetNumaNodeProcessorMask</a> function.


#### Examples

For an example, see <a href="/windows/desktop/Memory/allocating-memory-from-a-numa-node">Allocating Memory from a NUMA Node</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-getnumanodeprocessormask">GetNumaNodeProcessorMask</a>



<a href="/windows/desktop/ProcThread/numa-support">NUMA Support</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>