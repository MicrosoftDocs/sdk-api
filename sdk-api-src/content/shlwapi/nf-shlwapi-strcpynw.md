---
UID: NF:shlwapi.StrCpyNW
title: StrCpyNW function (shlwapi.h)
description: Copies a specified number of characters from the beginning of one string to another.Note  Do not use this function or the StrNCpy macro.
helpviewer_keywords: ["StrCpyN","StrCpyN function [Windows Shell]","StrCpyNW","_win32_StrCpyN","shell.StrCpyN","shlwapi/StrCpyN","shlwapi/StrCpyNW"]
old-location: shell\StrCpyN.htm
tech.root: shell
ms.assetid: 7e21414d-0d82-40b9-b32f-5eaf351166da
ms.date: 12/05/2018
ms.keywords: StrCpyN, StrCpyN function [Windows Shell], StrCpyNW, _win32_StrCpyN, shell.StrCpyN, shlwapi/StrCpyN, shlwapi/StrCpyNW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StrCpyNW (Unicode)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - StrCpyNW
 - shlwapi/StrCpyNW
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
 - StrCpyN
 - StrCpyNW
---

# StrCpyNW function


## -description

Copies a specified number of characters from the beginning of one string to another.
<div class="alert"><b>Note</b>  Do not use this function or the <b>StrNCpy</b> macro. See Remarks for alternative functions.</div><div> </div>

## -parameters

### -param pszDst [out]

Type: <b>PTSTR</b>

A pointer to a buffer that, when this function returns successfully, receives the copied string. This buffer must be of sufficient size to hold the copied characters. This string is not guaranteed to be null-terminated.

### -param pszSrc [in]

Type: <b>PCTSTR</b>

A pointer to the null-terminated source string.

### -param cchMax

Type: <b>int</b>

The number of characters to be copied, including the terminating null character.

## -returns

Type: <b>PTSTR</b>

Returns a pointer to <i>pszDst</i>.

## -remarks

<b>Security Warning:  </b>Using this function incorrectly can compromise the security of your application. The copied string is not guaranteed to be null-terminated.  Consider using one of the following alternatives. <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbcopya">StringCbCopy</a>, <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbcopyexa">StringCbCopyEx</a>, <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbcopyna">StringCbCopyN</a>, <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbcopynexa">StringCbCopyNEx</a>, <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchcopya">StringCchCopy</a>, <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchcopyexa">StringCchCopyEx</a>, <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchcopyna">StringCchCopyN</a>, <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchcopynexa">StringCchCopyNEx</a>. You should review <a href="/windows/desktop/shell/sec-shell">Security Considerations: Microsoft Windows Shell</a> before continuing.