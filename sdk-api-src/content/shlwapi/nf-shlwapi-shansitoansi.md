---
UID: NF:shlwapi.SHAnsiToAnsi
title: SHAnsiToAnsi function (shlwapi.h)
description: Copies an ANSI string.
helpviewer_keywords: ["SHAnsiToAnsi","SHAnsiToAnsi function [Windows Shell]","_win32_SHAnsiToAnsi","shell.SHAnsiToAnsi","shlwapi/SHAnsiToAnsi"]
old-location: shell\SHAnsiToAnsi.htm
tech.root: shell
ms.assetid: e57142ca-3098-4118-aac0-89724f711872
ms.date: 12/05/2018
ms.keywords: SHAnsiToAnsi, SHAnsiToAnsi function [Windows Shell], _win32_SHAnsiToAnsi, shell.SHAnsiToAnsi, shlwapi/SHAnsiToAnsi
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server, Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHAnsiToAnsi
 - shlwapi/SHAnsiToAnsi
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-DownLevel-shlwapi-l2-1-0.dll
 - ShCore.dll
 - API-MS-Win-DownLevel-shlwapi-l2-1-1.dll
 - API-MS-Win-ShCore-unicodeansi-l1-1-0.dll
api_name:
 - SHAnsiToAnsi
---

# SHAnsiToAnsi function


## -description

<p class="CCE_Message">[This function is available through Windows XP and Windows Server 2003. It might be altered or unavailable in subsequent versions of Windows.]

Copies an ANSI string.

## -parameters

### -param pszSrc [in]

Type: <b>LPCSTR</b>

A pointer to a null-terminated ANSI string to be converted to Unicode.

### -param pszDst [out]

Type: <b>LPWSTR</b>

A pointer to a buffer that, when this function returns successfully, receives the characters copied from <i>pszSrc</i>. The buffer must be large enough to contain the number of characters specified by the <i>cchBuf</i> parameter, including a room for a terminating null character.

### -param cchBuf

Type: <b>int</b>

The number of characters that can be contained by the buffer pointed to by <i>pszDst</i>. This parameter must be greater than zero.

## -returns

Type: <b>int</b>

Returns the number of characters written to <i>pszDst</i>, including the terminating null character. Returns 0 if unsuccessful.

## -remarks

<b>Security Warning:  </b>Using this function incorrectly can compromise the security of your application. For example, if <i>pszDst</i> buffer is not large enough to contain the number of characters specified by <i>cchBuf</i>, a buffer overrun can occur. Buffer overruns can cause a denial of service attack against an application if an access violation occurs. In the worst case, a buffer overrun might allow an attacker to inject executable code into your process, especially if <i>pszDst</i> is a stack-based buffer. Note that the output string is silently truncated if the buffer is not large enough. This can result in canonicalization or other security vulnerabilities.

If the <i>pszDst</i> buffer is not large enough to contain the entire converted output string, the string is truncated to fit the buffer. There is no way to detect that the return string has been truncated. The string will always be null-terminated, even if it has been truncated. This function takes care to not truncate between the lead and trail bytes of a DBCS character pair. In that case, only cchBuf-1 characters are returned.

If the <i>pszSrc</i> and <i>pszDst</i> buffers overlap, the function's behavior is undefined.

<div class="alert"><b>Note</b>  Do not assume that the function has not changed any of the characters in the output buffer that follow the string's terminating null character. The contents of the output buffer following the string's terminating null character are undefined, up to and including the last character in the buffer.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbcopya">StringCbCopy</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbcopyexa">StringCbCopyEx</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbcopyna">StringCbCopyN</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbcopynexa">StringCbCopyNEx</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcblengtha">StringCbLength</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchcopya">StringCchCopy</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchcopyexa">StringCchCopyEx</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchcopyna">StringCchCopyN</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchcopynexa">StringCchCopyNEx</a>



<b>StringCchLength</b>