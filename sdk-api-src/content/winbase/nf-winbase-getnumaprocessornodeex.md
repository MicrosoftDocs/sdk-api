---
UID: NF:winbase.GetNumaProcessorNodeEx
title: GetNumaProcessorNodeEx function (winbase.h)
description: Retrieves the node number as a USHORT value for the specified logical processor.
helpviewer_keywords: ["GetNumaProcessorNodeEx","GetNumaProcessorNodeEx function","base.getnumaprocessornodeex","winbase/GetNumaProcessorNodeEx"]
old-location: base\getnumaprocessornodeex.htm
tech.root: backup
ms.assetid: 6b843cd8-eeb5-4aa1-aad4-ce98916346b1
ms.date: 12/05/2018
ms.keywords: GetNumaProcessorNodeEx, GetNumaProcessorNodeEx function, base.getnumaprocessornodeex, winbase/GetNumaProcessorNodeEx
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
 - GetNumaProcessorNodeEx
 - winbase/GetNumaProcessorNodeEx
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
 - GetNumaProcessorNodeEx
---

# GetNumaProcessorNodeEx function


## -description

Retrieves the node number as a <b>USHORT</b> value for the specified logical processor.

## -parameters

### -param Processor [in]

A pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-processor_number">PROCESSOR_NUMBER</a> structure that represents the logical processor and the processor group to which it is assigned.

### -param NodeNumber [out]

A pointer  to a variable to receive the node number. If the specified processor does not exist, this parameter is set to MAXUSHORT.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

To compile an application that uses this function, set _WIN32_WINNT &gt;= 0x0601. For more information, see <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-getnumaprocessornode">GetNumaProcessorNode</a>



<a href="/windows/desktop/api/winnt/ns-winnt-processor_number">PROCESSOR_NUMBER</a>