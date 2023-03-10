---
UID: NF:winbase.GetNamedPipeClientSessionId
title: GetNamedPipeClientSessionId function (winbase.h)
description: Retrieves the client session identifier for the specified named pipe.
helpviewer_keywords: ["GetNamedPipeClientSessionId","GetNamedPipeClientSessionId function","base.getnamedpipeclientsessionid","winbase/GetNamedPipeClientSessionId"]
old-location: base\getnamedpipeclientsessionid.htm
tech.root: base
ms.assetid: b3ea0b7f-fead-4369-b87a-2f522a2a1984
ms.date: 12/05/2018
ms.keywords: GetNamedPipeClientSessionId, GetNamedPipeClientSessionId function, base.getnamedpipeclientsessionid, winbase/GetNamedPipeClientSessionId
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
 - GetNamedPipeClientSessionId
 - winbase/GetNamedPipeClientSessionId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - GetNamedPipeClientSessionId
---

# GetNamedPipeClientSessionId function


## -description

Retrieves the client session identifier for the specified named pipe.

## -parameters

### -param Pipe [in]

A handle to an instance of a named pipe. This handle must be created by the 
<a href="/windows/desktop/api/winbase/nf-winbase-createnamedpipea">CreateNamedPipe</a> function.

### -param ClientSessionId [out]

The session identifier.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -remarks

<b>Windows 10, version 1709:  </b>Pipes are only supported within an app-container; ie, from one UWP process to another UWP process that's part of the same app. Also, named pipes must use the syntax `\\.\pipe\LOCAL\` for the pipe name.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-createnamedpipea">CreateNamedPipe</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getnamedpipeserversessionid">GetNamedPipeServerSessionId</a>



<a href="/windows/desktop/ipc/pipe-functions">Pipe Functions</a>



<a href="/windows/desktop/ipc/pipes">Pipes Overview</a>