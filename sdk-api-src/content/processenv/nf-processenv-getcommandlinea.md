---
UID: NF:processenv.GetCommandLineA
title: GetCommandLineA function (processenv.h)
description: Retrieves the command-line string for the current process. (ANSI)
helpviewer_keywords: ["GetCommandLineA", "processenv/GetCommandLineA"]
old-location: base\getcommandline.htm
tech.root: backup
ms.assetid: 08dfcab2-eb6e-49a4-80eb-87d4076c98c6
ms.date: 10/23/2024
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
 - GetCommandLineA
 - processenv/GetCommandLineA
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

# GetCommandLineA function

## -description

Retrieves the command-line string for the current process.

## -returns

The return value is a pointer to the command-line string for the current process.

## -remarks

The lifetime of the returned value is managed by the system, applications should not free or modify this value.

Console processes can use the *argc* and *argv* arguments of the **main** or **wmain** functions by implementing those as the program entry point.

GUI processes can use the *lpCmdLine* argument of the [WinMain or wWinMain functions](../winbase/nf-winbase-winmain.md) by implementing those as the program entry point.

To convert the command line to an *argv* style array of strings, pass the result from GetCommandLineA to [CommandLineToArgvW](../shellapi/nf-shellapi-commandlinetoargvw.md).

> [!NOTE]
> The name of the executable in the command line that the operating system provides to a process is not necessarily identical to that in the command line that the calling process gives to the [CreateProcessA function](../processthreadsapi/nf-processthreadsapi-createprocessa.md). The operating system may prepend a fully qualified path to an executable name that is provided without a fully qualified path.

### Security Remarks

The command line returned by GetCommandLineA is a conversion of the Unicode command line to the 8-bit process code page.

For most code pages this conversion is lossy and the converted command line can differ from the Unicode command line, creating possible security issues like the following:

* The conversion may alter strings intended for use as file names. For example, if the ANSI code page is Windows-1252, the Unicode character U+0100 (Latin capital letter A with macron: &#x0100;) converts to 0x41 (the Latin capital letter A). If a user passes a file name containing the character &#x0100;, a program that uses GetCommandLineA will receive it with the character A and operate on the wrong file.
* The conversion may alter how the command line is parsed. For example, if the ANSI code page is Windows-1252, the Unicode character U+FF02 (Fullwidth quotation mark: &#xff02;) converts to 0x22 (the ASCII quotation mark) and the Unicode character U+2010 (Hyphen: &#x2010;) converts to 0x2D (the ASCII minus sign). Both of these can result in command line file arguments being misinterpreted as command line options.

To avoid this problem, use the GetCommandLineW function to receive the Unicode command line, or use an application manifest (on Windows Version 1903 or later) to [set UTF-8 as the process code page](/windows/apps/design/globalizing/use-utf8-code-page).

> [!NOTE]
> The processenv.h header defines GetCommandLine as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

[CreateProcessA function](../processthreadsapi/nf-processthreadsapi-createprocessa.md)

[Process and Thread Functions](/windows/desktop/ProcThread/process-and-thread-functions)
