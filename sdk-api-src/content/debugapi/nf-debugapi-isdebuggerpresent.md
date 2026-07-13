---
UID: NF:debugapi.IsDebuggerPresent
title: IsDebuggerPresent function (debugapi.h)
description: Determines whether the calling process is being debugged by a user-mode debugger.
helpviewer_keywords: ["IsDebuggerPresent","IsDebuggerPresent function","_win32_isdebuggerpresent","base.isdebuggerpresent","debugapi/IsDebuggerPresent"]
old-location: base\isdebuggerpresent.htm
tech.root: Debug
ms.assetid: 7bc4bcb7-3f85-4349-a1da-c4ebee2d3e3f
ms.date: 12/05/2018
ms.keywords: IsDebuggerPresent, IsDebuggerPresent function, _win32_isdebuggerpresent, base.isdebuggerpresent, debugapi/IsDebuggerPresent
req.header: debugapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows NT Workstation 4.0 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows NT Server 4.0 [desktop apps \| UWP apps]
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
 - IsDebuggerPresent
 - debugapi/IsDebuggerPresent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-debug-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-debug-l1-1-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Debug-L1-1-2.dll
api_name:
 - IsDebuggerPresent
---

# IsDebuggerPresent function


## -description

Determines whether the calling process is being debugged by a user-mode debugger.



## -returns

If the current process is running in the context of a debugger, the return value is nonzero.

If the current process is not running in the context of a debugger, the return value is zero.

## -remarks

This function allows an application to determine whether or not it is being debugged, so that it can modify its behavior. For example, an application could provide additional information using the 
<a href="/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw">OutputDebugString</a> function if it is being debugged.

To determine whether a remote process is being debugged, use the <a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent">CheckRemoteDebuggerPresent</a> function.

## -see-also

<a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent">CheckRemoteDebuggerPresent</a>



<a href="/windows/desktop/Debug/debugging-functions">Debugging Functions</a>



<a href="/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw">OutputDebugString</a>
