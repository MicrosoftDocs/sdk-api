---
UID: NF:wtsapi32.WTSTerminateProcess
title: WTSTerminateProcess function (wtsapi32.h)
description: Terminates the specified process on the specified Remote Desktop Session Host (RD Session Host) server.
helpviewer_keywords: ["WTSTerminateProcess","WTSTerminateProcess function [Remote Desktop Services]","_win32_wtsterminateprocess","termserv.wtsterminateprocess","wtsapi32/WTSTerminateProcess"]
old-location: termserv\wtsterminateprocess.htm
tech.root: TermServ
ms.assetid: 38036657-4e65-4100-893a-e35cf0b71e0d
ms.date: 12/05/2018
ms.keywords: WTSTerminateProcess, WTSTerminateProcess function [Remote Desktop Services], _win32_wtsterminateprocess, termserv.wtsterminateprocess, wtsapi32/WTSTerminateProcess
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wtsapi32.lib
req.dll: Wtsapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WTSTerminateProcess
 - wtsapi32/WTSTerminateProcess
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wtsapi32.dll
api_name:
 - WTSTerminateProcess
---

# WTSTerminateProcess function


## -description

Terminates the specified process on the specified Remote Desktop Session Host (RD Session Host) server.

## -parameters

### -param hServer [in]

Handle to an RD Session Host server. Specify a handle opened by the 
<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsopenservera">WTSOpenServer</a> function, or specify WTS_CURRENT_SERVER_HANDLE to indicate the RD Session Host server on which your application is running.

### -param ProcessId [in]

Specifies the process identifier of the process to terminate.

### -param ExitCode [in]

Specifies the exit code for the terminated process.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsopenservera">WTSOpenServer</a>