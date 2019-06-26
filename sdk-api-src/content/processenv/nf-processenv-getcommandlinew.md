---
UID: NF:processenv.GetCommandLineW
title: GetCommandLineW function (processenv.h)
author: windows-sdk-content
description: Retrieves the command-line string for the current process.
old-location: base\getcommandline.htm
tech.root: ProcThread
ms.assetid: 08dfcab2-eb6e-49a4-80eb-87d4076c98c6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetCommandLine, GetCommandLine function, GetCommandLineA, GetCommandLineW, _win32_getcommandline, base.getcommandline, processenv/GetCommandLine, processenv/GetCommandLineA, processenv/GetCommandLineW, winbase/GetCommandLine, winbase/GetCommandLineA, winbase/GetCommandLineW
ms.topic: function
f1_keywords: 
 - "processenv/GetCommandLine"
req.header: processenv.h
req.include-header: Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetCommandLineW function


## -description


Retrieves the command-line string for the current process.


## -parameters






## -returns



The return value is a pointer to the command-line string for the current process.




## -remarks



ANSI console processes written in C can use the <i>argc</i> and <i>argv</i> arguments of the <b>main</b> function to access the command-line arguments. ANSI GUI applications can use the <i>lpCmdLine</i> parameter of the <a href="_win32_WinMain_cpp">WinMain</a> function to access the command-line string, excluding the program name. The <b>main</b> and <b>WinMain</b> functions cannot return Unicode strings.

Unicode console process written in C can use the <b>wmain</b> or <b>_tmain</b> function to access the command-line arguments. Unicode GUI applications must use the 
<b>GetCommandLineW</b> function to access Unicode strings.

To convert the command line to an <i>argv</i> style array of strings, call the 
<a href="_shell_commandlinetoargvw">CommandLineToArgvW</a> function.

<div class="alert"><b>Note</b>  The name of the executable in the command line that the operating system provides to a process is not necessarily identical to that in the command line that the calling process gives to the 
<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a> function. The operating system may prepend a fully qualified path to an executable name that is provided without a fully qualified path.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>



<a href="https://docs.microsoft.com/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>
 

 

