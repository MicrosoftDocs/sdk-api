---
UID: NF:tlhelp32.Process32First
title: Process32First function (tlhelp32.h)
description: The Process32First function (tlhelp32.h) retrieves information about the first process encountered in a system snapshot.
helpviewer_keywords: ["Process32First","Process32First function [ToolHelp]","Process32FirstW","_win32_process32first","base.process32first","tlhelp32/Process32First","tlhelp32/Process32FirstW","toolhelp.process32first"]
old-location: toolhelp\process32first.htm
tech.root: ToolHelp
ms.assetid: 097790e8-30c2-4b00-9256-fa26e2ceb893
ms.date: 08/05/2022
ms.keywords: Process32First, Process32First function [ToolHelp], Process32FirstW, _win32_process32first, base.process32first, tlhelp32/Process32First, tlhelp32/Process32FirstW, toolhelp.process32first
req.header: tlhelp32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: Process32FirstW (Unicode) and Process32First (ANSI)
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
 - Process32First
 - tlhelp32/Process32First
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
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-toolhelp-l1-1-0.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
 - API-MS-Win-Core-ToolHelp-L1-1-1.dll
api_name:
 - Process32First
 - Process32First
 - Process32FirstW
---

# Process32First function


## -description

Retrieves information about the first process encountered in a system snapshot.

## -parameters

### -param hSnapshot [in]

A handle to the snapshot returned from a previous call to the 
<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-createtoolhelp32snapshot">CreateToolhelp32Snapshot</a> function.

### -param lppe [in, out]

A pointer to a 
<a href="/windows/desktop/api/tlhelp32/ns-tlhelp32-processentry32">PROCESSENTRY32</a> structure. It contains process information such as the name of the executable file, the process identifier, and the process identifier of the parent process.

## -returns

Returns <b>TRUE</b> if the first entry of the process list has been copied to the buffer or <b>FALSE</b> otherwise. The <b>ERROR_NO_MORE_FILES</b> error value is returned by the 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function if no processes exist or the snapshot does not contain process information.

## -remarks

The calling application must set the <b>dwSize</b> member of 
<a href="/windows/desktop/api/tlhelp32/ns-tlhelp32-processentry32">PROCESSENTRY32</a> to the size, in bytes, of the structure. 


To retrieve information about other processes recorded in the same snapshot, use the 
<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-process32next">Process32Next</a> function.


#### Examples

For an example, see 
<a href="/windows/desktop/ToolHelp/taking-a-snapshot-and-viewing-processes">Taking a Snapshot and Viewing Processes</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-createtoolhelp32snapshot">CreateToolhelp32Snapshot</a>



<a href="/windows/desktop/api/tlhelp32/ns-tlhelp32-processentry32">PROCESSENTRY32</a>



<a href="/windows/desktop/ToolHelp/process-walking">Process Walking</a>



<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-process32next">Process32Next</a>



<a href="/windows/desktop/ToolHelp/tool-help-functions">Tool Help Functions</a>
