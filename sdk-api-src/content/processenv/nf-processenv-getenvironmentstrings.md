---
UID: NF:processenv.GetEnvironmentStrings
title: GetEnvironmentStrings function (processenv.h)
author: windows-sdk-content
description: Retrieves the environment variables for the current process.
old-location: base\getenvironmentstrings.htm
tech.root: ProcThread
ms.assetid: fb431d83-f3e7-4f2a-bad9-81259681c1f4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetEnvironmentStrings, GetEnvironmentStrings function, GetEnvironmentStringsA, GetEnvironmentStringsW, _win32_getenvironmentstrings, base.getenvironmentstrings, processenv/GetEnvironmentStrings, processenv/GetEnvironmentStringsA, processenv/GetEnvironmentStringsW, winbase/GetEnvironmentStrings, winbase/GetEnvironmentStringsA, winbase/GetEnvironmentStringsW
ms.topic: function
req.header: processenv.h
req.include-header: Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetEnvironmentStringsW (Unicode) and GetEnvironmentStringsA (ANSI)
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
 - GetEnvironmentStrings
 - GetEnvironmentStringsA
 - GetEnvironmentStringsW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetEnvironmentStrings function


## -description


Retrieves the environment variables for the current process.


## -parameters






## -returns



If the function succeeds, the return value is a pointer to the environment block of the current process.

If the function fails, the return value is NULL.




## -remarks



The 
<b>GetEnvironmentStrings</b> function returns a pointer to a block of memory that contains the environment variables of the calling process (both the system and the user environment variables). Each environment block contains the environment variables in the following format:

<i>Var1</i>
<i>Value1</i>
<i>Var2</i>
<i>Value2</i>
<i>Var3</i>
<i>Value3</i>
<i>VarN</i>
<i>ValueN</i>
Treat this memory as read-only; do not modify it directly. To add or change an environment variable, use the 
<a href="https://msdn.microsoft.com/1d4cc328-12e6-4aae-9f58-58675116ad54">GetEnvironmentVariable</a> and 
<a href="https://msdn.microsoft.com/95bd6fa5-886d-41dc-a5c3-ede86dbfa15d">SetEnvironmentVariable</a> functions.

When the block returned by 
<b>GetEnvironmentStrings</b> is no longer needed, it should be freed by calling the 
<a href="https://msdn.microsoft.com/8ac73f6e-4b42-4730-bf88-4b671f57b63b">FreeEnvironmentStrings</a> function.

Note that the ANSI version of this function, <b>GetEnvironmentStringsA</b>, returns OEM characters.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/b428688c-7b16-48c7-8d89-55d066496d1c">Changing Environment Variables</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/6732b12f-ced1-4769-b947-79da8fd2237a">Environment Variables</a>



<a href="https://msdn.microsoft.com/8ac73f6e-4b42-4730-bf88-4b671f57b63b">FreeEnvironmentStrings</a>



<a href="https://msdn.microsoft.com/1d4cc328-12e6-4aae-9f58-58675116ad54">GetEnvironmentVariable</a>



<a href="https://msdn.microsoft.com/95bd6fa5-886d-41dc-a5c3-ede86dbfa15d">SetEnvironmentVariable</a>
 

 

