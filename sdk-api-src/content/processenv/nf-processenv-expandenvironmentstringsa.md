---
UID: NF:processenv.ExpandEnvironmentStringsA
title: ExpandEnvironmentStringsA function (processenv.h)
description: Expands environment-variable strings and replaces them with the values defined for the current user. (ANSI)
helpviewer_keywords: ["ExpandEnvironmentStringsA", "processenv/ExpandEnvironmentStringsA"]
old-location: base\expandenvironmentstrings.htm
tech.root: winprog
ms.assetid: b563e8ed-311d-4971-94f3-9c9fde4a2f30
ms.date: 12/05/2018
ms.keywords: ExpandEnvironmentStrings, ExpandEnvironmentStrings function, ExpandEnvironmentStringsA, ExpandEnvironmentStringsW, _win32_expandenvironmentstrings, base.expandenvironmentstrings, processenv/ExpandEnvironmentStrings, processenv/ExpandEnvironmentStringsA, processenv/ExpandEnvironmentStringsW
req.header: processenv.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ExpandEnvironmentStringsW (Unicode) and ExpandEnvironmentStringsA (ANSI)
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
 - ExpandEnvironmentStringsA
 - processenv/ExpandEnvironmentStringsA
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
 - ExpandEnvironmentStrings
 - ExpandEnvironmentStringsA
 - ExpandEnvironmentStringsW
---

# ExpandEnvironmentStringsA function


## -description

Expands environment-variable strings and replaces them with the values defined for the current user.

To specify the environment block for a particular user or the system, use the <a href="/windows/win32/api/userenv/nf-userenv-expandenvironmentstringsforusera">ExpandEnvironmentStringsForUser</a> function.

## -parameters

### -param lpSrc [in]

A buffer that contains one or more environment-variable strings in the form: %<i>variableName</i>%. For each such reference, the %<i>variableName</i>% portion is replaced with the current value of that environment variable. 




Case is ignored when looking up the environment-variable name. If the name is not found, the %<i>variableName</i>% portion is left unexpanded.

Note that this function does not support all the features that Cmd.exe supports. For example, it does not support %<i>variableName</i>:<i>str1</i>=<i>str2</i>% or %<i>variableName</i>:~<i>offset</i>,<i>length</i>%.

### -param lpDst [out, optional]

A pointer to a buffer that receives the result of expanding the environment variable strings in the <i>lpSrc</i> buffer. Note that this buffer cannot be the same as the <i>lpSrc</i> buffer.

### -param nSize [in]

The maximum number of characters that can be stored in the buffer pointed to by the <i>lpDst</i> parameter. When using ANSI strings, the buffer size should be the string length, plus terminating null character, plus one. When using Unicode strings, the buffer size should be the string length plus the terminating null character.

## -returns

If the function succeeds, the return value is the number of <b>TCHARs</b> stored in the destination buffer, including the terminating null character. If the destination buffer is too small to hold the expanded string, the return value is the required buffer size, in characters.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

**Windows Server 2003 and Windows XP:** The size of the <i>lpSrc</i> and <i>lpDst</i> buffers is limited to 32K.

To replace folder names in a fully qualified path with their associated environment-variable strings, use the <a href="/windows/desktop/api/shlwapi/nf-shlwapi-pathunexpandenvstringsa">PathUnExpandEnvStrings</a> function.

To retrieve the list of environment variables for a process, use the <a href="/windows/win32/api/processenv/nf-processenv-getenvironmentstrings">GetEnvironmentStrings</a> function.


#### Examples

For an example, see 
<a href="/windows/desktop/SysInfo/getting-system-information">Getting System Information</a>.

<div class="code"></div>




> [!NOTE]
> The processenv.h header defines ExpandEnvironmentStrings as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/ProcThread/environment-variables">Environment Variables</a>



<a href="/windows/desktop/SysInfo/system-information-functions">System
		  Information Functions</a>
