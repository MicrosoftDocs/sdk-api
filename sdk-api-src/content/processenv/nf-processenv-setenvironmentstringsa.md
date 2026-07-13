---
UID: NF:processenv.SetEnvironmentStringsA
title: SetEnvironmentStringsA
description: The SetEnvironmentStringsA function (processenv.h) sets the environment strings of the calling process for the current process.
ms.date: 07/18/2025
ms.keywords: SetEnvironmentStringsA
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
 - SetEnvironmentStringsA
 - processenv/SetEnvironmentStringsA
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - api-ms-win-core-processenvironment-ansi-l1-1-0.dll
 - kernel32.dll
 - api-ms-win-core-processenvironment-l1-1-0.dll
 - kernelbase.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
api_name:
 - SetEnvironmentStringsA
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

If the function fails, the return value is zero. To get extended error information, call [GetLastError](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## -remarks

## -see-also

[Environment Variables](/windows/desktop/ProcThread/environment-variables)
[GetEnvironmentStrings](/windows/win32/api/processenv/nf-processenv-getenvironmentstrings)
[GetEnvironmentVariable](../winbase/nf-winbase-getenvironmentvariable.md)
[SetEnvironmentVariable](../winbase/nf-winbase-setenvironmentvariable.md)
