---
UID: NF:processenv.SetEnvironmentVariableW
title: SetEnvironmentVariableW function (processenv.h)
description: The SetEnvironmentVariableW (Unicode) function (processenv.h) sets the contents of the specified environment variable for the current process. 
helpviewer_keywords: ["SetEnvironmentVariable", "SetEnvironmentVariable function", "SetEnvironmentVariableW", "_win32_setenvironmentvariable", "base.setenvironmentvariable", "processenv/SetEnvironmentVariable", "processenv/SetEnvironmentVariableW"]
old-location: base\setenvironmentvariable.htm
tech.root: backup
ms.assetid: 95bd6fa5-886d-41dc-a5c3-ede86dbfa15d
ms.date: 08/05/2022
ms.keywords: SetEnvironmentVariable, SetEnvironmentVariable function, SetEnvironmentVariableA, SetEnvironmentVariableW, _win32_setenvironmentvariable, base.setenvironmentvariable, processenv/SetEnvironmentVariable, processenv/SetEnvironmentVariableA, processenv/SetEnvironmentVariableW, winbase/SetEnvironmentVariable, winbase/SetEnvironmentVariableA, winbase/SetEnvironmentVariableW
req.header: processenv.h
req.include-header: Windows.h on Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetEnvironmentVariableW (Unicode) and SetEnvironmentVariableA (ANSI)
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
 - SetEnvironmentVariableW
 - processenv/SetEnvironmentVariableW
dev_langs:
 - c++
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
 - SetEnvironmentVariable
 - SetEnvironmentVariableA
 - SetEnvironmentVariableW
---

# SetEnvironmentVariableW function


## -description

Sets the contents of the specified environment variable for the current process.

## -parameters

### -param lpName [in]

The name of the environment variable. The operating system creates the environment variable if it does not exist and <i>lpValue</i> is not NULL.

### -param lpValue [in, optional]

The contents of the environment variable. 

The maximum size of a user-defined environment variable is 32,767 characters. There is no technical limitation on the size of the environment block. However, there are practical limits depending on the mechanism used to access the block. For example, a batch file cannot set a variable that is longer than the maximum command line length. For more information, see [Environment Variables](/windows/desktop/ProcThread/environment-variables).

<b>Windows Server 2003 and Windows XP:  </b>The total size of the environment block for a process may not exceed 32,767 characters.

If this parameter is NULL, the variable is deleted from the current process's environment.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function has no effect on the system environment variables or the environment variables of other processes.


#### Examples

For an example, see 
<a href="/windows/desktop/ProcThread/changing-environment-variables">Changing Environment Variables</a>.

<div class="code"></div>




> [!NOTE]
> The processenv.h header defines SetEnvironmentVariable as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/ProcThread/environment-variables">Environment Variables</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getenvironmentvariable">GetEnvironmentVariable</a>
