---
UID: NF:namedpipeapi.GetNamedPipeClientComputerNameW
tech.root: base 
title: GetNamedPipeClientComputerNameW
description: The GetNamedPipeClientComputerNameW (Unicode) function (winbase.h) retrieves the client computer name for the specified named pipe.
ms.date: 08/05/2022
targetos: Windows 
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Kernel32.dll 
req.header: namedpipeapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Kernel32.lib 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps] 
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps] 
req.target-type: Windows 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
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
 - GetNamedPipeClientComputerNameW
 - GetNamedPipeClientComputerName
f1_keywords:
 - GetNamedPipeClientComputerNameW
 - namedpipeapi/GetNamedPipeClientComputerNameW
 - GetNamedPipeClientComputerName
 - namedpipeapi/GetNamedPipeClientComputerName
dev_langs:
 - c++
---

# GetNamedPipeClientComputerNameW function

## -description

Retrieves the client computer name for the specified named pipe.

## -parameters

### -param Pipe [in]

A handle to an instance of a named pipe. This handle must be created by the 
<a href="/windows/desktop/api/namedpipeapi/nf-namedpipeapi-createnamedpipew">CreateNamedPipe</a> function.

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

<a href="/windows/desktop/api/namedpipeapi/nf-namedpipeapi-createnamedpipew">CreateNamedPipe</a>  
<a href="/windows/desktop/ipc/pipe-functions">Pipe Functions</a>  
<a href="/windows/desktop/ipc/pipes">Pipes Overview</a>  
