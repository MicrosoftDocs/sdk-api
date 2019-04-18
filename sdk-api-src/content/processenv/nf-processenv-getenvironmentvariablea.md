---
UID: NF:processenv.GetEnvironmentVariableA
title: GetEnvironmentVariableA function (processenv.h)
author: windows-sdk-content
description: Retrieves the contents of the specified variable from the environment block of the calling process.
old-location: base\getenvironmentvariable.htm
tech.root: ProcThread
ms.assetid: 1d4cc328-12e6-4aae-9f58-58675116ad54
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetEnvironmentVariable, GetEnvironmentVariable function, GetEnvironmentVariableA, GetEnvironmentVariableW, _win32_getenvironmentvariable, base.getenvironmentvariable, processenv/GetEnvironmentVariable, processenv/GetEnvironmentVariableA, processenv/GetEnvironmentVariableW, winbase/GetEnvironmentVariable, winbase/GetEnvironmentVariableA, winbase/GetEnvironmentVariableW
ms.topic: function
req.header: processenv.h
req.include-header: Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetEnvironmentVariableW (Unicode) and GetEnvironmentVariableA (ANSI)
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
 - GetEnvironmentVariable
 - GetEnvironmentVariableA
 - GetEnvironmentVariableW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetEnvironmentVariableA function


## -description


Retrieves the contents of the specified variable from the environment block of the calling process.


## -parameters




### -param lpName [in, optional]

The name of the environment variable.


### -param lpBuffer [out, optional]

A pointer to a buffer that receives the contents of the specified environment variable as a null-terminated string. An environment variable has a maximum size limit of 32,767 characters, including the null-terminating character.


### -param nSize [in]

The size of the buffer pointed to by the <i>lpBuffer</i> parameter, including the null-terminating character, in characters.


## -returns



If the function succeeds, the return value is the number of characters stored in the buffer pointed to by <i>lpBuffer</i>, not including the terminating null character.

If <i>lpBuffer</i> is not large enough to hold the data, the return value is the buffer size, in characters, required to hold the string and its terminating null character and the contents of <i>lpBuffer</i> are undefined.

If the function fails, the return value is zero. If the specified environment variable was not found in the environment block, 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns ERROR_ENVVAR_NOT_FOUND.




## -remarks



This function can retrieve either a system environment variable or a user environment variable.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/b428688c-7b16-48c7-8d89-55d066496d1c">Changing Environment Variables</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/6732b12f-ced1-4769-b947-79da8fd2237a">Environment Variables</a>



<a href="https://msdn.microsoft.com/fb431d83-f3e7-4f2a-bad9-81259681c1f4">GetEnvironmentStrings</a>



<a href="https://msdn.microsoft.com/95bd6fa5-886d-41dc-a5c3-ede86dbfa15d">SetEnvironmentVariable</a>
 

 

