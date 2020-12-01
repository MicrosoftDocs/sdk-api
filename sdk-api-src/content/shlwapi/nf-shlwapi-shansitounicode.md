---
UID: NF:shlwapi.SHAnsiToUnicode
title: SHAnsiToUnicode function (shlwapi.h)
description: Converts a string from the ANSI code page to the Unicode code page.
helpviewer_keywords: ["SHAnsiToUnicode","SHAnsiToUnicode function [Windows Shell]","_win32_SHAnsiToUnicode","shell.SHAnsiToUnicode","shlwapi/SHAnsiToUnicode"]
old-location: shell\SHAnsiToUnicode.htm
tech.root: shell
ms.assetid: 9578f26e-56ea-4f3b-b024-b2e285d0c4d2
ms.date: 12/05/2018
ms.keywords: SHAnsiToUnicode, SHAnsiToUnicode function [Windows Shell], _win32_SHAnsiToUnicode, shell.SHAnsiToUnicode, shlwapi/SHAnsiToUnicode
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
 - SHAnsiToUnicode
 - shlwapi/SHAnsiToUnicode
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
 - SHAnsiToUnicode
---

# SHAnsiToUnicode function


## -description

<p class="CCE_Message">[This function is available through Windows XP and Windows Server 2003. It might be altered or unavailable in subsequent versions of Windows.]

Converts a string from the ANSI code page to the Unicode code page.

## -parameters

### -param pszSrc [in]

Type: <b>PCSTR</b>

A pointer to a null-terminated ANSI string to be converted to Unicode.

### -param pwszDst [out]

Type: <b>PWSTR</b>

A pointer to a buffer that, when this function returns successfully, receives the string specified by <i>pszSrc</i>, after the ANSI characters have been converted to Unicode (WCHAR). The buffer must be large enough to contain the number of Unicode characters specified by the <i>cwchBuf</i> parameter, including a terminating null character.

### -param cwchBuf

Type: <b>int</b>

The number of Unicode characters that can be contained by the buffer pointed to by <i>pwszDst</i>. This parameter must be greater than zero.

## -returns

Type: <b>int</b>

Returns the number of Unicode characters written to <i>pwszDst</i>, including the terminating null character. Returns 0 if unsuccessful.

## -remarks

<b>Security Warning:  </b>Using this function incorrectly can compromise the security of your application. For example, if <i>pwszDst</i> buffer is not large enough to contain the number of characters specified by <i>cwchBuf</i>, a buffer overrun can occur. Buffer overruns can cause a denial of service attack against an application if an access violation occurs. In the worst case, a buffer overrun might allow an attacker to inject executable code into your process, especially if <i>pwszDst</i> is a stack-based buffer. When copying an entire string, note that sizeof returns the number of bytes, which is not the correct value to use for the <i>cwchBuf</i> parameter. Instead, use sizeof(pwszDst)/sizeof(WCHAR). Note that this technique assumes that <i>pwszDst</i> is an array, not a pointer.

If the <i>pwszDst</i> buffer is not large enough to contain the entire converted output string, the string is truncated to fit the buffer. There is no way to detect that the return string has been truncated.  The string is always null-terminated, even if it has been truncated. This ensures that no more than <i>cwchBuf</i> characters are copied to <i>pwszDst</i>. No attempt is made to avoid truncating the string in the middle of a Unicode surrogate pair.

If the <i>pszSrc</i> and <i>pwszDst</i> buffers overlap, the function's behavior is undefined.

<div class="alert"><b>Note</b>  Do not assume that the function has not changed any of the characters in the output buffer that follow the string's terminating null character. The contents of the output buffer following the string's terminating null character are undefined, up to and including the last character in the buffer.</div>
<div> </div>
<b>SHAnsiToTChar</b> is defined to be the same as <b>SHAnsiToUnicode</b>.

## -see-also

<a href="/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar">MultiByteToWideChar</a>



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