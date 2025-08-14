---
UID: NF:winbase.GetNumaAvailableMemoryNodeEx
title: GetNumaAvailableMemoryNodeEx function (winbase.h)
description: Retrieves the amount of memory that is available in a node specified as a USHORT value.
helpviewer_keywords: ["GetNumaAvailableMemoryNodeEx","GetNumaAvailableMemoryNodeEx function","base.getnumaavailablememorynodeex","winbase/GetNumaAvailableMemoryNodeEx"]
old-location: base\getnumaavailablememorynodeex.htm
tech.root: backup
ms.assetid: 59382114-f3da-45e0-843e-51c0fd52a164
ms.date: 12/05/2018
ms.keywords: GetNumaAvailableMemoryNodeEx, GetNumaAvailableMemoryNodeEx function, base.getnumaavailablememorynodeex, winbase/GetNumaAvailableMemoryNodeEx
req.header: winbase.h
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
 - GetNumaAvailableMemoryNodeEx
 - winbase/GetNumaAvailableMemoryNodeEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-kernel32-legacy-l1-1-6.dll
 - kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - GetNumaAvailableMemoryNodeEx
---

# GetNumaAvailableMemoryNodeEx function


## -description

Retrieves the amount of memory that is available in a node specified as a <b>USHORT</b> value.

## -parameters

### -param Node [in]

The number of the node.

### -param AvailableBytes [out]

The amount of available memory for the node, in bytes.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>GetNumaAvailableMemoryNodeEx</b> function returns the amount of memory consumed by free and zeroed pages on the specified node. On systems with more than one node, this memory does not include standby pages. Therefore, the sum of the available memory values for all nodes in the system is equal to the value of the Free &amp; Zero Page List Bytes memory performance counter. On systems with only one node, the value returned by <a href="/windows/desktop/api/winbase/nf-winbase-getnumaavailablememorynode">GetNumaAvailableMemoryNode</a>  includes standby pages and  is equal to the value of the Available Bytes memory performance counter. For more information about performance counters, see <a href="/previous-versions/windows/desktop/legacy/aa965225(v=vs.85)">Memory Performance Information</a>.

The only difference between the <b>GetNumaAvailableMemoryNodeEx</b> function and the <a href="/windows/desktop/api/winbase/nf-winbase-getnumaavailablememorynode">GetNumaAvailableMemoryNode</a> function is the data type of the <i>Node</i> parameter. 

To compile an application that uses this function, set _WIN32_WINNT &gt;= 0x0601. For more information, see <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-getnumaavailablememorynode">GetNumaAvailableMemoryNode</a>



<a href="/windows/desktop/ProcThread/numa-support">NUMA Support</a>