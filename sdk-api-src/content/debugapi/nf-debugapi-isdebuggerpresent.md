---
UID: NF:debugapi.IsDebuggerPresent
title: IsDebuggerPresent function (debugapi.h)
author: windows-sdk-content
description: Determines whether the calling process is being debugged by a user-mode debugger.
old-location: base\isdebuggerpresent.htm
tech.root: Debug
ms.assetid: 7bc4bcb7-3f85-4349-a1da-c4ebee2d3e3f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IsDebuggerPresent, IsDebuggerPresent function, _win32_isdebuggerpresent, base.isdebuggerpresent, debugapi/IsDebuggerPresent
ms.topic: function
req.header: debugapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - API-MS-Win-Core-debug-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-debug-l1-1-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Debug-L1-1-2.dll
api_name:
 - IsDebuggerPresent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IsDebuggerPresent function


## -description


Determines whether the calling process is being debugged by a user-mode debugger.


## -parameters






## -returns



If the current process is running in the context of a debugger, the return value is nonzero.

If the current process is not running in the context of a debugger, the return value is zero.




## -remarks



This function allows an application to determine whether or not it is being debugged, so that it can modify its behavior. For example, an application could provide additional information using the 
<a href="https://msdn.microsoft.com/ca23d9a9-65b7-4a36-bd09-857a6997f482">OutputDebugString</a> function if it is being debugged.

To determine whether a remote process is being debugged, use the <a href="https://msdn.microsoft.com/e7eb2d48-4ef3-4708-8895-2bc33d2c3e91">CheckRemoteDebuggerPresent</a> function.

To compile an application that uses this function, define the _WIN32_WINNT macro as 0x0400 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/e7eb2d48-4ef3-4708-8895-2bc33d2c3e91">CheckRemoteDebuggerPresent</a>



<a href="https://msdn.microsoft.com/95a838a2-f138-4682-b733-3f363b6c4a4b">Debugging Functions</a>



<a href="https://msdn.microsoft.com/ca23d9a9-65b7-4a36-bd09-857a6997f482">OutputDebugString</a>
 

 

