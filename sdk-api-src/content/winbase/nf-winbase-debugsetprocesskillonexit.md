---
UID: NF:winbase.DebugSetProcessKillOnExit
title: DebugSetProcessKillOnExit function (winbase.h)
description: Sets the action to be performed when the calling thread exits.
helpviewer_keywords: ["DebugSetProcessKillOnExit","DebugSetProcessKillOnExit function","_win32_debugsetprocesskillonexit","base.debugsetprocesskillonexit","winbase/DebugSetProcessKillOnExit"]
old-location: base\debugsetprocesskillonexit.htm
tech.root: Debug
ms.assetid: 7ef44527-bde4-41f0-a470-d3f404c77ea9
ms.date: 12/05/2018
ms.keywords: DebugSetProcessKillOnExit, DebugSetProcessKillOnExit function, _win32_debugsetprocesskillonexit, base.debugsetprocesskillonexit, winbase/DebugSetProcessKillOnExit
req.header: winbase.h
req.include-header: Windows.h
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DebugSetProcessKillOnExit
 - winbase/DebugSetProcessKillOnExit
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
 - DebugSetProcessKillOnExit
---

# DebugSetProcessKillOnExit function


## -description

Sets the action to be performed when the calling thread exits.

## -parameters

### -param KillOnExit [in]

If this parameter is <b>TRUE</b>, the thread terminates all attached processes on exit (note that this is the default). Otherwise, the thread detaches from all processes being debugged on exit.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The calling thread must have established at least one debugging connection using the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a> or <a href="/windows/desktop/api/debugapi/nf-debugapi-debugactiveprocess">DebugActiveProcess</a> function before calling this function. <b>DebugSetProcessKillOnExit</b> affects all current and future debuggees connected to the calling thread. A thread can call this function multiple times to change the action as needed.

## -see-also

<a href="/windows/desktop/api/debugapi/nf-debugapi-debugactiveprocessstop">DebugActiveProcessStop</a>



<a href="/windows/desktop/Debug/debugging-functions">Debugging Functions</a>