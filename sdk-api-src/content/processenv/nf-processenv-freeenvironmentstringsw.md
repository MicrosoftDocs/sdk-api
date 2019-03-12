---
UID: NF:processenv.FreeEnvironmentStringsW
title: FreeEnvironmentStringsW function
author: windows-sdk-content
description: Frees a block of environment strings.
old-location: base\freeenvironmentstrings.htm
tech.root: ProcThread
ms.assetid: 8ac73f6e-4b42-4730-bf88-4b671f57b63b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FreeEnvironmentStrings, FreeEnvironmentStrings function, FreeEnvironmentStringsA, FreeEnvironmentStringsW, _win32_freeenvironmentstrings, base.freeenvironmentstrings, processenv/FreeEnvironmentStrings, processenv/FreeEnvironmentStringsA, processenv/FreeEnvironmentStringsW, winbase/FreeEnvironmentStrings, winbase/FreeEnvironmentStringsA, winbase/FreeEnvironmentStringsW
ms.topic: function
req.header: processenv.h
req.include-header: Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FreeEnvironmentStringsW (Unicode) and FreeEnvironmentStringsA (ANSI)
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
 - API-MS-Win-Core-ProcessEnvironment-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-ProcessEnvironment-l1-2-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - FreeEnvironmentStrings
 - FreeEnvironmentStringsA
 - FreeEnvironmentStringsW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FreeEnvironmentStringsW function


## -description


Frees a block of environment strings.


## -parameters




### -param penv

TBD




#### - lpszEnvironmentBlock [in]

A pointer to a block of environment strings. The pointer to the block must be obtained by calling the 
<a href="https://msdn.microsoft.com/fb431d83-f3e7-4f2a-bad9-81259681c1f4">GetEnvironmentStrings</a> function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If you used the ANSI version of <a href="https://msdn.microsoft.com/fb431d83-f3e7-4f2a-bad9-81259681c1f4">GetEnvironmentStrings</a>, be sure to use the ANSI version of <b>FreeEnvironmentStrings</b>. Similarly, if you used the Unicode version of <b>GetEnvironmentStrings</b>, be sure to use the Unicode version of <b>FreeEnvironmentStrings</b>.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/b428688c-7b16-48c7-8d89-55d066496d1c">Changing Environment Variables</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/6732b12f-ced1-4769-b947-79da8fd2237a">Environment Variables</a>



<a href="https://msdn.microsoft.com/fb431d83-f3e7-4f2a-bad9-81259681c1f4">GetEnvironmentStrings</a>
 

 

