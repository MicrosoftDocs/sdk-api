---
UID: NF:processenv.FreeEnvironmentStringsA
title: FreeEnvironmentStringsA function (processenv.h)
description: Frees a block of environment strings. (ANSI)
helpviewer_keywords: ["FreeEnvironmentStringsA", "processenv/FreeEnvironmentStringsA"]
old-location: base\freeenvironmentstrings.htm
tech.root: backup
ms.assetid: 8ac73f6e-4b42-4730-bf88-4b671f57b63b
ms.date: 12/05/2018
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
 - FreeEnvironmentStringsA
 - processenv/FreeEnvironmentStringsA
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

# FreeEnvironmentStringsA function


## -description

Frees a block of environment strings.

## -parameters

### -param penv

A pointer to a block of environment strings. The pointer to the block must be obtained by calling the 
<a href="/windows/desktop/api/rrascfg/nf-rrascfg-ieapproviderconfig-initialize">GetEnvironmentStrings</a> function.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If you used the ANSI version of <a href="/windows/desktop/api/rrascfg/nf-rrascfg-ieapproviderconfig-initialize">GetEnvironmentStrings</a>, be sure to use the ANSI version of <b>FreeEnvironmentStrings</b>. Similarly, if you used the Unicode version of <b>GetEnvironmentStrings</b>, be sure to use the Unicode version of <b>FreeEnvironmentStrings</b>.


#### Examples

For an example, see 
<a href="/windows/desktop/ProcThread/changing-environment-variables">Changing Environment Variables</a>.

<div class="code"></div>




> [!NOTE]
> The processenv.h header defines FreeEnvironmentStrings as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/ProcThread/environment-variables">Environment Variables</a>



<a href="/windows/desktop/api/rrascfg/nf-rrascfg-ieapproviderconfig-initialize">GetEnvironmentStrings</a>
