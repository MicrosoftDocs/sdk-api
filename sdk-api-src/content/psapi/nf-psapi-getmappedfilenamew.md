---
UID: NF:psapi.GetMappedFileNameW
title: GetMappedFileNameW function (psapi.h)
description: Checks whether the specified address is within a memory-mapped file in the address space of the specified process. If so, the function returns the name of the memory-mapped file.helpviewer_keywords: ["GetMappedFileName","GetMappedFileName function [PSAPI]","GetMappedFileNameA","GetMappedFileNameW","K32GetMappedFileName","K32GetMappedFileNameA","K32GetMappedFileNameW","_win32_getmappedfilename","base.getmappedfilename","psapi.getmappedfilename","psapi/GetMappedFileName","psapi/GetMappedFileNameA","psapi/GetMappedFileNameW","psapi/K32GetMappedFileName","psapi/K32GetMappedFileNameA","psapi/K32GetMappedFileNameW"]
old-location: psapi\getmappedfilename.htm
tech.root: psapi
ms.assetid: 10a2e5ab-f495-486d-8ef7-ef763716afd1
ms.date: 12/05/2018
ms.keywords: GetMappedFileName, GetMappedFileName function [PSAPI], GetMappedFileNameA, GetMappedFileNameW, K32GetMappedFileName, K32GetMappedFileNameA, K32GetMappedFileNameW, _win32_getmappedfilename, base.getmappedfilename, psapi.getmappedfilename, psapi/GetMappedFileName, psapi/GetMappedFileNameA, psapi/GetMappedFileNameW, psapi/K32GetMappedFileName, psapi/K32GetMappedFileNameA, psapi/K32GetMappedFileNameW
f1_keywords:
- psapi/GetMappedFileName
dev_langs:
- c++
req.header: psapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetMappedFileNameW (Unicode) and GetMappedFileNameA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib on Windows 7 and Windows Server 2008 R2; Psapi.lib (if PSAPI_VERSION=1) on Windows 7 and Windows Server 2008 R2; Psapi.lib on Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP
req.dll: Kernel32.dll on Windows 7 and Windows Server 2008 R2; Psapi.dll (if PSAPI_VERSION=1) on Windows 7 and Windows Server 2008 R2; Psapi.dll on Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Kernel32.dll
- Psapi.dll
- Psapi.dll
- API-MS-Win-Core-PsAPI-Ansi-L1-1-0.dll
- API-MS-Win-Core-PsAPI-L1-1-0.dll
- KernelBase.dll
api_name:
- GetMappedFileName
- GetMappedFileNameA
- GetMappedFileNameW
- K32GetMappedFileName
- K32GetMappedFileNameW
- K32GetMappedFileNameA
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetMappedFileNameW function


## -description


Checks whether the specified address is within a memory-mapped file in the address space of the specified process. If so, the function returns the name of the memory-mapped file.


## -parameters




### -param hProcess [in]

A handle to the process. The handle must have the <b>PROCESS_QUERY_INFORMATION</b> and <b>PROCESS_VM_READ</b> access rights. For more information, see <a href="https://docs.microsoft.com/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.


### -param lpv [in]

The address to be verified.


### -param lpFilename [out]

A pointer to the buffer that receives the name of the memory-mapped file to which the address specified by <i>lpv</i> belongs.


### -param nSize [in]

The size of the <i>lpFilename</i> buffer, in characters.


## -returns



If the function succeeds, the return value specifies the length of the string copied to the buffer, in characters.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



Starting with Windows 7 and Windows Server 2008 R2, Psapi.h establishes 
    version numbers for the PSAPI functions. The PSAPI version number affects the name used to call the function and 
    the library that a program must load.

If <b>PSAPI_VERSION</b> is 2 or greater, this function is defined as 
    <b>K32GetMappedFileName</b> in Psapi.h and exported in 
    Kernel32.lib and Kernel32.dll. If <b>PSAPI_VERSION</b> is 1, this 
    function is defined as <b>GetMappedFileName</b> in 
    Psapi.h and exported in Psapi.lib and Psapi.dll as a wrapper that calls 
    <b>K32GetMappedFileName</b>. 

Programs that must run on earlier versions of Windows as 
    well as Windows 7 and later versions should always call this function as 
    <b>GetMappedFileName</b>. To ensure correct resolution of symbols, 
    add Psapi.lib to the <b>TARGETLIBS</b> macro and compile the program with 
    <b>-DPSAPI_VERSION=1</b>. To use run-time dynamic linking, load Psapi.dll.

In Windows Server 2012, this function is supported by the following technologies.

<table>
<tr>
<th>Technology</th>
<th>Supported</th>
</tr>
<tr>
<td>
Server Message Block (SMB) 3.0 protocol

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
SMB 3.0 Transparent Failover (TFO)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
SMB 3.0 with Scale-out File Shares (SO)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
Cluster Shared Volume File System (CsvFS)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
Resilient File System (ReFS)

</td>
<td>
Yes

</td>
</tr>
</table>
 


#### Examples

For an example, see 
<a href="https://docs.microsoft.com/windows/desktop/Memory/obtaining-a-file-name-from-a-file-handle">Obtaining a File Name From a File Handle</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/psapi/nf-psapi-enumprocesses">EnumProcesses</a>



<a href="https://docs.microsoft.com/windows/desktop/psapi/memory-mapped-file-information">Memory-Mapped File Information</a>



<a href="https://docs.microsoft.com/windows/desktop/psapi/psapi-functions">PSAPI Functions</a>
 

 

