---
UID: NF:processenv.ExpandEnvironmentStringsW
title: ExpandEnvironmentStringsW function (processenv.h)
description: Expands environment-variable strings and replaces them with the values defined for the current user.
helpviewer_keywords: ["ExpandEnvironmentStrings","ExpandEnvironmentStrings function","ExpandEnvironmentStringsA","ExpandEnvironmentStringsW","_win32_expandenvironmentstrings","base.expandenvironmentstrings","processenv/ExpandEnvironmentStrings","processenv/ExpandEnvironmentStringsA","processenv/ExpandEnvironmentStringsW"]
old-location: base\expandenvironmentstrings.htm
tech.root: SysInfo
ms.assetid: b563e8ed-311d-4971-94f3-9c9fde4a2f30
ms.date: 12/05/2018
ms.keywords: ExpandEnvironmentStrings, ExpandEnvironmentStrings function, ExpandEnvironmentStringsA, ExpandEnvironmentStringsW, _win32_expandenvironmentstrings, base.expandenvironmentstrings, processenv/ExpandEnvironmentStrings, processenv/ExpandEnvironmentStringsA, processenv/ExpandEnvironmentStringsW
f1_keywords:
- processenv/ExpandEnvironmentStrings
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ExpandEnvironmentStringsW function


## -description


Expands environment-variable strings and replaces them with the values defined for the current user.

To specify the environment block for a particular user or the system, use the <a href="/windows/win32/api/processenv/nf-processenv-expandenvironmentstringsw">ExpandEnvironmentStringsForUser</a> function.


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
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



The size of the <i>lpSrc</i> and <i>lpDst</i> buffers is limited to 32K.

To replace folder names in a fully qualified path with their associated environment-variable strings, use the <a href="https://docs.microsoft.com/windows/desktop/api/shlwapi/nf-shlwapi-pathunexpandenvstringsa">PathUnExpandEnvStrings</a> function.

To retrieve the list of environment variables for a process, use the <a href="https://docs.microsoft.com/windows/desktop/api/rrascfg/nf-rrascfg-ieapproviderconfig-initialize">GetEnvironmentStrings</a> function.


#### Examples

For an example, see 
<a href="https://docs.microsoft.com/windows/desktop/SysInfo/getting-system-information">Getting System Information</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/ProcThread/environment-variables">Environment Variables</a>



<a href="https://docs.microsoft.com/windows/desktop/SysInfo/system-information-functions">System
		  Information Functions</a>
 

 

