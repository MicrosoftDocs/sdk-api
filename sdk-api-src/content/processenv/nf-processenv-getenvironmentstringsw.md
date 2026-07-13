---
UID: NF:processenv.GetEnvironmentStringsW
title: GetEnvironmentStringsW function (processenv.h)
description: The GetEnvironmentStringsW (Unicode) function (processenv.h) retrieves the environment variables for the current process. 
helpviewer_keywords: ["GetEnvironmentStrings","GetEnvironmentStrings function","GetEnvironmentStringsA","GetEnvironmentStringsW","_win32_getenvironmentstrings","base.getenvironmentstrings","processenv/GetEnvironmentStrings","processenv/GetEnvironmentStringsA","processenv/GetEnvironmentStringsW","winbase/GetEnvironmentStrings","winbase/GetEnvironmentStringsA","winbase/GetEnvironmentStringsW"]
old-location: base\getenvironmentstrings.htm
tech.root: backup
ms.assetid: fb431d83-f3e7-4f2a-bad9-81259681c1f4
ms.date: 08/05/2022
ms.keywords: GetEnvironmentStrings, GetEnvironmentStrings function, GetEnvironmentStringsA, GetEnvironmentStringsW, _win32_getenvironmentstrings, base.getenvironmentstrings, processenv/GetEnvironmentStrings, processenv/GetEnvironmentStringsA, processenv/GetEnvironmentStringsW, winbase/GetEnvironmentStrings, winbase/GetEnvironmentStringsA, winbase/GetEnvironmentStringsW
req.header: processenv.h
req.include-header: Windows.h on Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetEnvironmentStringsW
 - processenv/GetEnvironmentStringsW
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
 - GetEnvironmentStrings
 - GetEnvironmentStringsA
 - GetEnvironmentStringsW
---

# GetEnvironmentStringsW function


## -description

Retrieves the environment variables for the current process.



## -returns

If the function succeeds, the return value is a pointer to the environment block of the current process.

If the function fails, the return value is NULL.

## -remarks

The 
<b>GetEnvironmentStrings</b> function returns a pointer to a block of memory that contains the environment variables of the calling process (both the system and the user environment variables). Each environment block contains the environment variables in the following format:

*Var1*=*Value1*\0<br/>
*Var2*=*Value2*\0<br/>
*Var3*=*Value3*\0<br/>
...<br/>
*VarN*=*ValueN*\0\0

The name of an environment variable cannot include an equal sign (=).

Treat this memory as read-only; do not modify it directly. To add or change an environment variable, use the 
<a href="/windows/desktop/api/winbase/nf-winbase-getenvironmentvariable">GetEnvironmentVariable</a> and 
<a href="/windows/desktop/api/winbase/nf-winbase-setenvironmentvariable">SetEnvironmentVariable</a> functions.

When the block returned by 
<b>GetEnvironmentStrings</b> is no longer needed, it should be freed by calling the 
<a href="/windows/desktop/api/processenv/nf-processenv-freeenvironmentstringsa">FreeEnvironmentStrings</a> function.

Note that the ANSI version of this function, <b>GetEnvironmentStringsA</b>, returns OEM characters.


#### Examples

For an example, see 
<a href="/windows/desktop/ProcThread/changing-environment-variables">Changing Environment Variables</a>.

<div class="code"></div>




> [!NOTE]
> The processenv.h header defines GetEnvironmentStrings as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/ProcThread/environment-variables">Environment Variables</a>



<a href="/windows/desktop/api/processenv/nf-processenv-freeenvironmentstringsa">FreeEnvironmentStrings</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getenvironmentvariable">GetEnvironmentVariable</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setenvironmentvariable">SetEnvironmentVariable</a>
