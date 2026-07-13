---
UID: NF:processenv.FreeEnvironmentStringsW
title: FreeEnvironmentStringsW function (processenv.h)
description: Frees a block of environment strings. (Unicode)
helpviewer_keywords: ["FreeEnvironmentStrings", "FreeEnvironmentStrings function", "FreeEnvironmentStringsW", "_win32_freeenvironmentstrings", "base.freeenvironmentstrings", "processenv/FreeEnvironmentStrings", "processenv/FreeEnvironmentStringsW"]
old-location: base\freeenvironmentstrings.htm
tech.root: backup
ms.assetid: 8ac73f6e-4b42-4730-bf88-4b671f57b63b
ms.date: 12/02/2024
ms.keywords: FreeEnvironmentStrings, FreeEnvironmentStrings function, FreeEnvironmentStringsA, FreeEnvironmentStringsW, _win32_freeenvironmentstrings, base.freeenvironmentstrings, processenv/FreeEnvironmentStrings, processenv/FreeEnvironmentStringsA, processenv/FreeEnvironmentStringsW, winbase/FreeEnvironmentStrings, winbase/FreeEnvironmentStringsA, winbase/FreeEnvironmentStringsW
req.header: processenv.h
req.include-header: Windows.h on Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FreeEnvironmentStringsW
 - processenv/FreeEnvironmentStringsW
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
 - FreeEnvironmentStrings
 - FreeEnvironmentStringsA
 - FreeEnvironmentStringsW
---

# FreeEnvironmentStringsW function

## -description

Frees a block of environment strings.

## -parameters

### -param penv

A pointer to a block of environment strings. The pointer to the block must be obtained by calling the [GetEnvironmentStringsW](nf-processenv-getenvironmentstringsw.md) function.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call [GetLastError](../errhandlingapi/nf-errhandlingapi-getlasterror.md).

## -remarks

If you used the ANSI version of [GetEnvironmentStrings](nf-processenv-getenvironmentstrings.md), be sure to use the ANSI version of **FreeEnvironmentStrings**. Similarly, if you used the Unicode version of **GetEnvironmentStrings**, be sure to use the Unicode version of **FreeEnvironmentStrings**.


### Examples

For an example, see [Changing Environment Variables](/windows/win32/procthread/changing-environment-variables).

> [!NOTE]
> The processenv.h header defines FreeEnvironmentStrings as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

[Environment Variables](/windows/win32/procthread/environment-variables)

[GetEnvironmentStrings](nf-processenv-getenvironmentstrings.md)
