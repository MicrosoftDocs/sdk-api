---
UID: NF:shlwapi.wvnsprintfW
title: wvnsprintfW function (shlwapi.h)
description: Takes a list of arguments and returns the values of the arguments as a printf-style formatted string. (Unicode)
helpviewer_keywords: ["_win32_wvnsprintf", "shell.wvnsprintf", "shlwapi/wvnsprintf", "shlwapi/wvnsprintfW", "wvnsprintf", "wvnsprintf function [Windows Shell]", "wvnsprintfW"]
old-location: shell\wvnsprintf.htm
tech.root: shell
ms.assetid: a2aaaa05-d61e-41e3-8e49-7c0da1a661f0
ms.date: 12/05/2018
ms.keywords: _win32_wvnsprintf, shell.wvnsprintf, shlwapi/wvnsprintf, shlwapi/wvnsprintfA, shlwapi/wvnsprintfW, wvnsprintf, wvnsprintf function [Windows Shell], wvnsprintfA, wvnsprintfW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: wvnsprintfW (Unicode) and wvnsprintfA (ANSI)
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
 - wvnsprintfW
 - shlwapi/wvnsprintfW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
api_name:
 - wvnsprintf
 - wvnsprintfA
 - wvnsprintfW
---

# wvnsprintfW function


## -description

Takes a list of arguments and returns the values of the arguments as a <a href="/windows/desktop/direct3dhlsl/printf">printf</a>-style formatted string.
            
<div class="alert"><b>Note</b>  Do not use this function. See Remarks for alternative functions.</div><div> </div>

## -parameters

### -param pszDest [out]

Type: <b>PTSTR</b>

A pointer to a buffer that, when this function returns successfully, receives the output string.

### -param cchDest [in]

Type: <b>int</b>

The maximum number of characters allowed in <i>pszDest</i>.

### -param pszFmt [in]

Type: <b>PCTSTR</b>

A <a href="cpp/c-runtime-library/reference/printf-printf-l-wprintf-wprintf-l">printf</a>-style format string. The %s format identifier should never be used in an unbounded form. To avoid potential buffer overruns, always specify a size; for instance "%32s".

### -param arglist [in]

Type: <b>va_list</b>

A pointer to a list of command-line parameters used to customize the output.

## -returns

Type: <b>int</b>

Returns the number of characters written to the buffer, excluding any terminating <b>NULL</b> characters. A negative value is returned if an error occurs.

## -remarks

<b>Security Warning:  </b>Using this function incorrectly can compromise the security of your application. The copied string is not guaranteed to be null-terminated. Consider using one of the following alternatives. <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbprintfa">StringCbPrintf</a>, <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbprintfexa">StringCbPrintfEx</a>, <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbvprintfa">StringCbVPrintf</a>, <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbvprintfexa">StringCbVPrintfEx</a>, <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa">StringCchPrintf</a>, <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfexa">StringCchPrintfEx</a>, <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchvprintfa">StringCchVPrintf</a>, or <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchvprintfexa">StringCchVPrintfEx</a>. You should review <a href="/windows/desktop/shell/sec-shell">Security Considerations: Microsoft Windows Shell</a> before continuing.




> [!NOTE]
> The shlwapi.h header defines wvnsprintf as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
