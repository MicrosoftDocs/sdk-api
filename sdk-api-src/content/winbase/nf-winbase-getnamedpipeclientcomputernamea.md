---
UID: NF:winbase.GetNamedPipeClientComputerNameA
title: GetNamedPipeClientComputerNameA function (winbase.h)
description: The GetNamedPipeClientComputerNameA (ANSI) function (winbase.h) retrieves the client computer name for the specified named pipe.
helpviewer_keywords: ["GetNamedPipeClientComputerName","GetNamedPipeClientComputerName function","GetNamedPipeClientComputerNameA","GetNamedPipeClientComputerNameW","base.getnamedpipeclientcomputername","winbase/GetNamedPipeClientComputerName","winbase/GetNamedPipeClientComputerNameA","winbase/GetNamedPipeClientComputerNameW"]
old-location: base\getnamedpipeclientcomputername.htm
tech.root: base
ms.assetid: 8daa97fe-0ef7-4ada-a99c-aff487ad27e5
ms.date: 08/04/2022
ms.keywords: GetNamedPipeClientComputerName, GetNamedPipeClientComputerName function, GetNamedPipeClientComputerNameA, GetNamedPipeClientComputerNameW, base.getnamedpipeclientcomputername, winbase/GetNamedPipeClientComputerName, winbase/GetNamedPipeClientComputerNameA, winbase/GetNamedPipeClientComputerNameW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetNamedPipeClientComputerNameW (Unicode) and GetNamedPipeClientComputerNameA (ANSI)
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
 - GetNamedPipeClientComputerNameA
 - winbase/GetNamedPipeClientComputerNameA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-NamedPipe-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-NamedPipe-l1-2-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-NamedPipe-l1-2-1.dll
 - API-Ms-Win-Core-Namedpipe-Ansi-L1-1-0.dll
 - Kernel32Legacy.dll
 - API-MS-Win-Core-NamedPipe-Ansi-L1-1-1.dll
 - API-MS-Win-Core-NamedPipe-L1-2-2.dll
api_name:
 - GetNamedPipeClientComputerName
 - GetNamedPipeClientComputerNameA
 - GetNamedPipeClientComputerNameW
---

# GetNamedPipeClientComputerNameA function


## -description

Retrieves the client computer name for the specified named pipe.

## -parameters

### -param Pipe [in]

A handle to an instance of a named pipe. This handle must be created by the 
<a href="/windows/desktop/api/winbase/nf-winbase-createnamedpipea">CreateNamedPipe</a> function.

### -param ClientComputerName [out]

The computer name.

### -param ClientComputerNameLength [in]

The size of the <i>ClientComputerName</i> buffer, in bytes.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -remarks

<b>Windows 10, version 1709:  </b>Pipes are only supported within an app-container; ie, from one UWP process to another UWP process that's part of the same app. Also, named pipes must use the syntax `\\.\pipe\LOCAL\` for the pipe name.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-createnamedpipea">CreateNamedPipe</a>



<a href="/windows/desktop/ipc/pipe-functions">Pipe Functions</a>



<a href="/windows/desktop/ipc/pipes">Pipes Overview</a>