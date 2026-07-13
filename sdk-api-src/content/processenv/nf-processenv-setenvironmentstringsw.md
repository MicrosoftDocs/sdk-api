---
UID: NF:processenv.SetEnvironmentStringsW
title: SetEnvironmentStringsW
description: The SetEnvironmentStringsW (Unicode) function (processenv.h) sets the environment strings of the calling process for the current process.
ms.date: 10/31/2024
ms.keywords: SetEnvironmentStringsW
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: kernel32.dll
req.header: processenv.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: kernel32.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - SetEnvironmentStringsW
 - processenv/SetEnvironmentStringsW
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - api-ms-win-core-processenvironment-l1-2-0.dll
 - kernel32.dll
 - api-ms-win-core-processenvironment-l1-1-0.dll
 - kernelbase.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
api_name:
 - SetEnvironmentStringsW
---

## -description

Sets the environment strings of the calling process (both the system and the user environment variables) for the current process.

## -parameters

### -param NewEnvironment

The environment variable string using the following format:

*Var1*=*Value1*\0<br/>
*Var2*=*Value2*\0<br/>
*Var3*=*Value3*\0<br/>
...<br/>
*VarN*=*ValueN*\0\0

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

## -see-also
<a href="/windows/desktop/ProcThread/environment-variables">Environment Variables</a>

<a href="/windows/win32/api/processenv/nf-processenv-getenvironmentstrings">GetEnvironmentStrings</a>

<a href="/windows/desktop/api/winbase/nf-winbase-getenvironmentvariable">GetEnvironmentVariable</a>

<a href="/windows/desktop/api/winbase/nf-winbase-setenvironmentvariable">SetEnvironmentVariable</a>
