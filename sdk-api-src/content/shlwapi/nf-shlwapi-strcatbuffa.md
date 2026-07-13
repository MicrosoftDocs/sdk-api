---
UID: NF:shlwapi.StrCatBuffA
title: StrCatBuffA function (shlwapi.h)
description: Copies and appends characters from one string to the end of another. (ANSI)
helpviewer_keywords: ["StrCatBuffA", "shlwapi/StrCatBuffA"]
old-location: shell\StrCatBuff.htm
tech.root: shell
ms.assetid: ce8c002f-f4f8-4b5f-a9e2-7bcd21f8808c
ms.date: 12/05/2018
ms.keywords: StrCatBuff, StrCatBuff function [Windows Shell], StrCatBuffA, StrCatBuffW, _win32_StrCatBuff, shell.StrCatBuff, shlwapi/StrCatBuff, shlwapi/StrCatBuffA, shlwapi/StrCatBuffW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StrCatBuffW (Unicode) and StrCatBuffA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - StrCatBuffA
 - shlwapi/StrCatBuffA
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
 - StrCatBuff
 - StrCatBuffA
 - StrCatBuffW
---

# StrCatBuffA function


## -description

Copies and appends characters from one string to the end of another.
            
<div class="alert"><b>Note</b>  Do not use. See Remarks for alternative functions.</div><div> </div>

## -parameters

### -param pszDest [in, out]

Type: <b>PTSTR</b>

A pointer to a null-terminated string. When this function returns successfully, this string contains its original content with the string <i>pszSrc</i> appended.

### -param pszSrc [in]

Type: <b>PCTSTR</b>

A pointer to the string to be appended to <i>pszDest</i>.

### -param cchDestBuffSize

Type: <b>int</b>

The size of the buffer, in characters, pointed to by <i>pszDest</i>. This value must be at least the length of the combined string plus the terminating null character. If the buffer is too small to fit the entire string, the string will be truncated.

## -returns

Type: <b>PTSTR</b>

Returns a pointer to the destination string.

## -remarks

<b>Security Warning:  </b>Using this function incorrectly can compromise the security of your application. The final string is not guaranteed to be null-terminated. Consider using one of the following alternatives: <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbcata">StringCbCat</a>, <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbcatexa">StringCbCatEx</a>, <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbcatna">StringCbCatN</a>, <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbcatnexa">StringCbCatNEx</a>, <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchcata">StringCchCat</a>, <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchcatexa">StringCchCatEx</a>, <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchcatna">StringCchCatN</a>, or <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchcatnexa">StringCchCatNEx</a>. You should review <a href="/windows/desktop/shell/sec-shell">Security Considerations: Microsoft Windows Shell</a> before continuing.




> [!NOTE]
> The shlwapi.h header defines StrCatBuff as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
