---
UID: NF:debugapi.CheckRemoteDebuggerPresent
title: CheckRemoteDebuggerPresent function (debugapi.h)
author: windows-sdk-content
description: Determines whether the specified process is being debugged.
old-location: base\checkremotedebuggerpresent.htm
tech.root: Debug
ms.assetid: e7eb2d48-4ef3-4708-8895-2bc33d2c3e91
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CheckRemoteDebuggerPresent, CheckRemoteDebuggerPresent function, base.checkremotedebuggerpresent, debugapi/CheckRemoteDebuggerPresent
ms.topic: function
req.header: debugapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP1 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-debug-l1-1-1.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Debug-L1-1-2.dll
api_name:
 - CheckRemoteDebuggerPresent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CheckRemoteDebuggerPresent function


## -description


Determines whether the specified process is being debugged.


## -parameters




### -param hProcess [in]

A handle to the process.


### -param pbDebuggerPresent [in, out]

A pointer to a variable that the function sets to <b>TRUE</b> if the specified process is being debugged, or <b>FALSE</b> otherwise.


## -returns



If the function succeeds, the return value is nonzero. 

If the function fails, the return value is zero. To get  extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The "remote" in <b>CheckRemoteDebuggerPresent</b> does not imply that the debugger  necessarily resides on a different computer; instead, it indicates that the debugger resides in a separate and parallel process. Use the <a href="https://msdn.microsoft.com/7bc4bcb7-3f85-4349-a1da-c4ebee2d3e3f">IsDebuggerPresent</a> function to detect whether the calling process is running under the debugger.

To compile an application that uses this function, define the _WIN32_WINNT macro as 0x0501 or later. For more information, see <a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/95a838a2-f138-4682-b733-3f363b6c4a4b">Debugging Functions</a>



<a href="https://msdn.microsoft.com/7bc4bcb7-3f85-4349-a1da-c4ebee2d3e3f">IsDebuggerPresent</a>
 

 

