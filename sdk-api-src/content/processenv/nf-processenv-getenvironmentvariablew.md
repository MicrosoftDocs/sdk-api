---
UID: NF:processenv.GetEnvironmentVariableW
title: GetEnvironmentVariableW function (processenv.h)
description: Retrieves the contents of the specified variable from the environment block of the calling process.
helpviewer_keywords: ["GetEnvironmentVariable","GetEnvironmentVariable function","GetEnvironmentVariableA","GetEnvironmentVariableW","_win32_getenvironmentvariable","base.getenvironmentvariable","processenv/GetEnvironmentVariable","processenv/GetEnvironmentVariableA","processenv/GetEnvironmentVariableW","winbase/GetEnvironmentVariable","winbase/GetEnvironmentVariableA","winbase/GetEnvironmentVariableW"]
old-location: base\getenvironmentvariable.htm
tech.root: backup
ms.assetid: 1d4cc328-12e6-4aae-9f58-58675116ad54
ms.date: 12/05/2018
ms.keywords: GetEnvironmentVariable, GetEnvironmentVariable function, GetEnvironmentVariableA, GetEnvironmentVariableW, _win32_getenvironmentvariable, base.getenvironmentvariable, processenv/GetEnvironmentVariable, processenv/GetEnvironmentVariableA, processenv/GetEnvironmentVariableW, winbase/GetEnvironmentVariable, winbase/GetEnvironmentVariableA, winbase/GetEnvironmentVariableW
f1_keywords:
- processenv/GetEnvironmentVariable
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetEnvironmentVariableW function


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
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_ENVVAR_NOT_FOUND.




## -remarks



This function can retrieve either a system environment variable or a user environment variable.


#### Examples

For an example, see 
<a href="https://docs.microsoft.com/windows/desktop/ProcThread/changing-environment-variables">Changing Environment Variables</a>.

<div class="code"></div>




> [!NOTE]
> The processenv.h header defines GetEnvironmentVariable as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also




<a href="https://docs.microsoft.com/windows/desktop/ProcThread/environment-variables">Environment Variables</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rrascfg/nf-rrascfg-ieapproviderconfig-initialize">GetEnvironmentStrings</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-setenvironmentvariable">SetEnvironmentVariable</a>
 

 

