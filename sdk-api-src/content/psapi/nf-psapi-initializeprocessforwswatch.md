---
UID: NF:psapi.InitializeProcessForWsWatch
title: InitializeProcessForWsWatch function (psapi.h)
description: Initiates monitoring of the working set of the specified process.
helpviewer_keywords: ["InitializeProcessForWsWatch","InitializeProcessForWsWatch function [PSAPI]","K32InitializeProcessForWatch","K32InitializeProcessForWsWatch","_win32_initializeprocessforwswatch","base.initializeprocessforwswatch","psapi.initializeprocessforwswatch","psapi/InitializeProcessForWsWatch","psapi/K32InitializeProcessForWsWatch"]
old-location: psapi\initializeprocessforwswatch.htm
tech.root: psapi
ms.assetid: c928656c-a59d-41b5-9434-911329b0278e
ms.date: 12/05/2018
ms.keywords: InitializeProcessForWsWatch, InitializeProcessForWsWatch function [PSAPI], K32InitializeProcessForWatch, K32InitializeProcessForWsWatch, _win32_initializeprocessforwswatch, base.initializeprocessforwswatch, psapi.initializeprocessforwswatch, psapi/InitializeProcessForWsWatch, psapi/K32InitializeProcessForWsWatch
req.header: psapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: Kernel32.lib on Windows 7 and Windows Server 2008 R2; Psapi.lib (if PSAPI_VERSION=1) on Windows 7 and Windows Server 2008 R2; Psapi.lib on Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP
req.dll: Kernel32.dll on Windows 7 and Windows Server 2008 R2; Psapi.dll (if PSAPI_VERSION=1) on Windows 7 and Windows Server 2008 R2; Psapi.dll on Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InitializeProcessForWsWatch
 - psapi/InitializeProcessForWsWatch
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - Psapi.dll
 - Psapi.dll
 - API-MS-Win-Core-PsAPI-L1-1-0.dll
 - KernelBase.dll
api_name:
 - InitializeProcessForWsWatch
 - K32InitializeProcessForWsWatch
---

# InitializeProcessForWsWatch function


## -description

Initiates monitoring of the working set of the specified process. You must call this function before calling the 
<a href="/windows/desktop/api/psapi/nf-psapi-getwschanges">GetWsChanges</a> function.

## -parameters

### -param hProcess [in]

A handle to the process. The handle must have the PROCESS_QUERY_INFORMATION access right. For more information, see <a href="/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Starting with Windows 7 and Windows Server 2008 R2, Psapi.h establishes 
    version numbers for the PSAPI functions. The PSAPI version number affects the name used to call the function and 
    the library that a program must load.

If <b>PSAPI_VERSION</b> is 2 or greater, this function is defined as 
    <b>K32InitializeProcessForWsWatch</b> in Psapi.h and exported in 
    Kernel32.lib and Kernel32.dll. If <b>PSAPI_VERSION</b> is 1, this 
    function is defined as <b>InitializeProcessForWsWatch</b> in 
    Psapi.h and exported in Psapi.lib and Psapi.dll as a wrapper that calls 
    <b>K32InitializeProcessForWsWatch</b>. 

Programs that must run on earlier versions of Windows as 
    well as Windows 7 and later versions should always call this function as 
    <b>InitializeProcessForWsWatch</b>. To ensure correct resolution of symbols, 
    add Psapi.lib to the <b>TARGETLIBS</b> macro and compile the program with 
    <b>-DPSAPI_VERSION=1</b>. To use run-time dynamic linking, load Psapi.dll.

## -see-also

<a href="/windows/desktop/api/psapi/nf-psapi-enumprocesses">EnumProcesses</a>



<a href="/windows/desktop/api/psapi/nf-psapi-getwschanges">GetWsChanges</a>



<a href="/windows/desktop/psapi/psapi-functions">PSAPI Functions</a>



<a href="/windows/desktop/psapi/working-set-information">Working Set Information</a>