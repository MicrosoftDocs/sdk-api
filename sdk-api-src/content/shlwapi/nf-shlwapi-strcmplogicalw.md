---
UID: NF:shlwapi.StrCmpLogicalW
title: StrCmpLogicalW function (shlwapi.h)
description: Compares two Unicode strings. Digits in the strings are considered as numerical content rather than text. This test is not case-sensitive.
helpviewer_keywords: ["StrCmpLogicalW","StrCmpLogicalW function [Windows Shell]","_shell_StrCmpLogicalW","shell.StrCmpLogicalW","shlwapi/StrCmpLogicalW"]
old-location: shell\StrCmpLogicalW.htm
tech.root: shell
ms.assetid: 013c6db3-7d14-44ef-89af-b3aac28f4e3f
ms.date: 12/05/2018
ms.keywords: StrCmpLogicalW, StrCmpLogicalW function [Windows Shell], _shell_StrCmpLogicalW, shell.StrCmpLogicalW, shlwapi/StrCmpLogicalW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StrCmpLogicalW (Unicode)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.5 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - StrCmpLogicalW
 - shlwapi/StrCmpLogicalW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-Core-shlwapi-Obsolete-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-shlwapi-Obsolete-l1-2-0.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-0.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-1.dll
api_name:
 - StrCmpLogicalW
 - StrCmpLogicalW
---

# StrCmpLogicalW function


## -description

Compares two Unicode strings. Digits in the strings are considered as numerical content rather than text. This test is not case-sensitive.

## -parameters

### -param psz1 [in]

Type: <b>PCWSTR</b>

A pointer to the first null-terminated string to be compared.

### -param psz2 [in]

Type: <b>PCWSTR</b>

A pointer to the second null-terminated string to be compared.

## -returns

Type: <b>int</b>

<ul>
<li>Returns zero if the strings are identical.</li>
<li>Returns 1 if the string pointed to by <i>psz1</i> has a greater value than that pointed to by <i>psz2</i>.</li>
<li>Returns -1 if the string pointed to by <i>psz1</i> has a lesser value than that pointed to by <i>psz2</i>.</li>
</ul>

## -remarks

This function's ordering schema differs somewhat from <a href="/windows/desktop/api/shlwapi/nf-shlwapi-strcmpiw">StrCmpI</a>, which also compares strings without regard to case sensitivity. Considering digits by their numerical value—as <b>StrCmpLogicalW</b> does—strings are ordered as follows:
		
                


```
2string
3string
20string
st2ring
st3ring
st20ring
string2
string3
string20
```


<b>StrCmpI</b> considers digits in the string only as text so that those same strings are ordered as follows:
		    
                


```
20string
2string
3string
st20ring
st2ring
st3ring
string2
string20
string3
```


<div class="alert"><b>Note</b>  Behavior of this function, and therefore the results it returns, can change from release to release. It should not be used for canonical sorting applications.</div>
<div> </div>