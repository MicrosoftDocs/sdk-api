---
UID: NF:shellapi.DoEnvironmentSubstA
title: DoEnvironmentSubstA function (shellapi.h)
description: Parses an input string that contains references to one or more environment variables and replaces them with their fully expanded values. (ANSI)
helpviewer_keywords: ["DoEnvironmentSubstA", "shellapi/DoEnvironmentSubstA"]
old-location: shell\DoEnvironmentSubst.htm
tech.root: shell
ms.assetid: cdf8bf2d-f446-4e0d-8664-bff2c45f74ec
ms.date: 12/05/2018
ms.keywords: DoEnvironmentSubst, DoEnvironmentSubst function [Windows Shell], DoEnvironmentSubstA, DoEnvironmentSubstW, _win32_DoEnvironmentSubst, shell.DoEnvironmentSubst, shellapi/DoEnvironmentSubst, shellapi/DoEnvironmentSubstA, shellapi/DoEnvironmentSubstW
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DoEnvironmentSubstW (Unicode) and DoEnvironmentSubstA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DoEnvironmentSubstA
 - shellapi/DoEnvironmentSubstA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - DoEnvironmentSubst
 - DoEnvironmentSubstA
 - DoEnvironmentSubstW
---

# DoEnvironmentSubstA function


## -description

<p class="CCE_Message">[This function is retained only for backward compatibility. Use <a href="/windows/win32/api/processenv/nf-processenv-expandenvironmentstringsa">ExpandEnvironmentStrings</a> instead.]

Parses an input string that contains references to one or more environment variables and replaces them with their fully expanded values.

## -parameters

### -param pszSrc [in, out]

Type: <b>LPTSTR</b>

A pointer to a null-terminated string that contains references to one or more environment variables, each in the following form. Case is ignored. 
    					
                        


``` syntax
%VariableName%
```

Any character in the string that is not enclosed in '%' characters is ignored and returned unchanged. Therefore, if your string contains multiple environment variables, you can use any character other than '%' as a separator, including spaces or no separator.

When this function returns successfully, each %<i>VariableName</i>% is replaced with its expanded value. The replacement rules are the same as those used by the command interpreter. If the variable name is not found on the system, the %<i>variableName</i>% is left as it was submitted on entry.

If this function fails due to the expanded string being too large for the buffer, the contents of this buffer are left unchanged.

### -param cchSrc

Type: <b>UINT</b>

The size, in characters, of the buffer pointed to by <i>pszSrc</i>. Note that the buffer must be large enough to hold the returned string.

## -returns

Type: <b>DWORD</b>

If the expanded string fits in the buffer, <b>TRUE</b> is returned in the HIWORD and the length, in characters, of the new <i>pszSrc</i> is returned in the LOWORD. 
                    
                        

If the expanded string is too large for the buffer, <b>FALSE</b> is returned in the HIWORD and <i>cchSrc</i> in the LOWORD.

## -remarks

Parameters must contain valid, non-<b>NULL</b> values. You must validate these values. Failure to do so can provide unexpected results.

Because the string that is returned in <i>pszSrc</i> will typically be longer than the input string, make sure that the buffer is large enough to hold the expanded version of the string. The allotted size of the <i>cchSrc</i> buffer for ANSI strings must be one larger than the buffer for a Unicode string. When dealing with ANSI strings, use the formula <i>buffer size = string length + terminating null character + 1</i> to determine the minimum correct buffer size.

Because environment variables can be added by the user or applications, the complete list is system-dependent. The following environment variables are standard and are available to both interactive applications and services.
    				
            	

<ul>
<li>ALLUSERSPROFILE</li>
<li>APPDATA</li>
<li>COMPUTERNAME</li>
<li>LOCALAPPDATA</li>
<li>NUMBER_OF_PROCESSORS</li>
<li>OS</li>
<li>PROCESSOR_ARCHITECTURE</li>
<li>PROCESSOR_IDENTIFIER</li>
<li>PROCESSOR_LEVEL</li>
<li>PROCESSOR_REVISION</li>
<li>ProgramData</li>
<li>ProgramFiles</li>
<li>PUBLIC</li>
<li>SystemDrive</li>
<li>SystemRoot</li>
<li>USERPROFILE</li>
<li>windir</li>
</ul>
The following are only available to interactive applications.

<ul>
<li>HOMEDRIVE</li>
<li>HOMEPATH</li>
<li>LOGONSERVER</li>
<li>USERDOMAIN</li>
<li>USERNAME</li>
</ul>
The environment variables that correspond to file system folders can be mapped to an equivalent <a href="/windows/desktop/shell/csidl">CSIDL</a> or <a href="/windows/desktop/shell/knownfolderid">KNOWNFOLDERID</a> value can be obtained through <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation">SHGetFolderLocation</a> or <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath">SHGetKnownFolderPath</a>. CSIDLs and KNOWNFOLDERIDs are more reliable than environment variable names and should be used whenever possible.


#### Examples

The following console application demonstrates the use of <b>DoEnvironmentSubstW</b>.


```cpp

#include "stdafx.h"
#include "windows.h"
#include "windef.h"
#include "shellapi.h"

int _tmain(int argc, _TCHAR* argv[])
{
	WCHAR szSrc[MAX_PATH] = L"%OS%;%HOMEPATH%";

	DWORD result = DoEnvironmentSubstW(szSrc, MAX_PATH);

	WORD success = HIWORD(result);
	WORD string_length = LOWORD(result);

	return 0;
}
```





> [!NOTE]
> The shellapi.h header defines DoEnvironmentSubst as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
