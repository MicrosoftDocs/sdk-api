---
UID: NF:processenv.GetCommandLineW
title: GetCommandLineW function (processenv.h)
description: Retrieves the command-line string for the current process. (Unicode)
helpviewer_keywords: ["GetCommandLine", "GetCommandLine function", "GetCommandLineW", "_win32_getcommandline", "base.getcommandline", "processenv/GetCommandLine", "processenv/GetCommandLineW"]
old-location: base\getcommandline.htm
tech.root: backup
ms.assetid: 08dfcab2-eb6e-49a4-80eb-87d4076c98c6
ms.date: 12/05/2018
ms.keywords: GetCommandLine, GetCommandLine function, GetCommandLineA, GetCommandLineW, _win32_getcommandline, base.getcommandline, processenv/GetCommandLine, processenv/GetCommandLineA, processenv/GetCommandLineW, winbase/GetCommandLine, winbase/GetCommandLineA, winbase/GetCommandLineW
req.header: processenv.h
req.include-header: Windows.h on Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetCommandLineW (Unicode) and GetCommandLineA (ANSI)
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
 - GetCommandLineW
 - processenv/GetCommandLineW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-ProcessEnvironment-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-ProcessEnvironment-l1-2-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - GetCommandLine
 - GetCommandLineA
 - GetCommandLineW
---

# GetCommandLineW function


## -description

Retrieves the command-line string for the current process.



## -returns

The return value is a pointer to the command-line string for the current process.

## -remarks

The lifetime of the returned value is managed by the system, applications should not free or modify this value.

Console processes can use the <i>argc</i> and <i>argv</i> arguments of the <b>main</b> or <b>wmain</b> functions by implementing those as the program entry point.
GUI processes can use the <i>lpCmdLine</i> argument of the <a href="/windows/win32/api/winbase/nf-winbase-winmain">WinMain</a> or wWinMain functions by implementing those as the program entry point.

To convert the command line to an <i>argv</i> style array of strings, pass the result from GetCommandLineW to
<a href="/windows/win32/api/shellapi/nf-shellapi-commandlinetoargvw">CommandLineToArgvW</a>.

<div class="alert"><b>Note</b>  The name of the executable in the command line that the operating system provides to a process is not necessarily identical to that in the command line that the calling process gives to the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a> function. The operating system may prepend a fully qualified path to an executable name that is provided without a fully qualified path.</div>
<div> </div>

> [!NOTE]
> The processenv.h header defines GetCommandLine as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>

<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>
