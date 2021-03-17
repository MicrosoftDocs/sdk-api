---
UID: NF:shlwapi.StrCatChainW
title: StrCatChainW function (shlwapi.h)
description: Concatenates two Unicode strings. Used when repeated concatenations to the same buffer are required.
helpviewer_keywords: ["StrCatChainW","StrCatChainW function [Windows Shell]","_shell_StrCatChainW","shell.StrCatChainW","shlwapi/StrCatChainW"]
old-location: shell\StrCatChainW.htm
tech.root: shell
ms.assetid: 8df35616-f6f3-45eb-9a83-89fc84938fd7
ms.date: 12/05/2018
ms.keywords: StrCatChainW, StrCatChainW function [Windows Shell], _shell_StrCatChainW, shell.StrCatChainW, shlwapi/StrCatChainW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StrCatChainW (Unicode)
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
 - StrCatChainW
 - shlwapi/StrCatChainW
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
 - StrCatChainW
 - StrCatChainW
---

# StrCatChainW function


## -description

Concatenates two Unicode strings. Used when repeated concatenations to the same buffer are required.

## -parameters

### -param pszDst [out]

Type: <b>PWSTR</b>

A pointer to a buffer that, when this function returns successfully, receives the null-terminated, Unicode string.

### -param cchDst

Type: <b>DWORD</b>

The size of the destination buffer, in characters. This buffer must be of sufficient size to hold both strings as well as a terminating null character. If the buffer is too small, the final string is truncated.

### -param ichAt

Type: <b>DWORD</b>

The offset into the destination buffer at which to begin the append action. If the string is not empty, set this value to -1 to have the current number of filled characters (not including the terminating null character) calculated for you.

### -param pszSrc [in]

Type: <b>PCWSTR</b>

A pointer to the null-terminated Unicode source string.

## -returns

Type: <b>DWORD</b>

Returns the offset of the null character after the last character added to <i>pszDst</i>.

## -remarks

<b>Security Warning:  </b>Using this function incorrectly can compromise the security of your application. The final string is not guaranteed to be null-terminated. Consider using one of the following alternatives: <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbcatexa">StringCbCatEx</a>, <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbcatnexa">StringCbCatNEx</a>, <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchcatexa">StringCchCatEx</a>, or <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchcatnexa">StringCchCatNEx</a>. You should review <a href="/windows/desktop/shell/sec-shell">Security Considerations: Microsoft Windows Shell</a> before continuing.