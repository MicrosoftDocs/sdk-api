---
UID: NF:winbase.GetNamedPipeClientProcessId
title: GetNamedPipeClientProcessId function (winbase.h)
description: Retrieves the client process identifier for the specified named pipe.
helpviewer_keywords: ["GetNamedPipeClientProcessId","GetNamedPipeClientProcessId function","base.getnamedpipeclientprocessid","winbase/GetNamedPipeClientProcessId"]
old-location: base\getnamedpipeclientprocessid.htm
tech.root: base
ms.assetid: 7001eb89-3d91-44e3-b245-b19e8ab5f9fe
ms.date: 12/05/2018
ms.keywords: GetNamedPipeClientProcessId, GetNamedPipeClientProcessId function, base.getnamedpipeclientprocessid, winbase/GetNamedPipeClientProcessId
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - GetNamedPipeClientProcessId
 - winbase/GetNamedPipeClientProcessId
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
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - GetNamedPipeClientProcessId
---

# GetNamedPipeClientProcessId function


## -description

Retrieves the client process identifier for the specified named pipe.

## -parameters

### -param Pipe [in]

A handle to an instance of a named pipe. This handle must be created by the 
<a href="/windows/desktop/api/winbase/nf-winbase-createnamedpipea">CreateNamedPipe</a> function.

### -param ClientProcessId [out]

The process identifier.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -remarks

<b>Windows 10, version 1709:  </b>Pipes are only supported within an app-container; ie, from one UWP process to another UWP process that's part of the same app. Also, named pipes must use the syntax `\\.\pipe\LOCAL\` for the pipe name.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-createnamedpipea">CreateNamedPipe</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getnamedpipeserverprocessid">GetNamedPipeServerProcessId</a>



<a href="/windows/desktop/ipc/pipe-functions">Pipe Functions</a>



<a href="/windows/desktop/ipc/pipes">Pipes Overview</a>