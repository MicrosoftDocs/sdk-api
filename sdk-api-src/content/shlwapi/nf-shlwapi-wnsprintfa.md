---
UID: NF:shlwapi.wnsprintfA
title: wnsprintfA function (shlwapi.h)
description: Takes a variable-length argument list and returns the values of the arguments as a printf-style formatted string.helpviewer_keywords: ["_win32_wnsprintf","shell.wnsprintf","shlwapi/wnsprintf","shlwapi/wnsprintfA","shlwapi/wnsprintfW","wnsprintf","wnsprintf function [Windows Shell]","wnsprintfA","wnsprintfW"]
old-location: shell\wnsprintf.htm
tech.root: shell
ms.assetid: 1d2b472b-6b34-4867-897c-eca60921d414
ms.date: 12/05/2018
ms.keywords: _win32_wnsprintf, shell.wnsprintf, shlwapi/wnsprintf, shlwapi/wnsprintfA, shlwapi/wnsprintfW, wnsprintf, wnsprintf function [Windows Shell], wnsprintfA, wnsprintfW
f1_keywords:
- shlwapi/wnsprintf
dev_langs:
- c++
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: wnsprintfW (Unicode) and wnsprintfA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Shlwapi.dll
api_name:
- wnsprintf
- wnsprintfA
- wnsprintfW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# wnsprintfA function


## -description


Takes a variable-length argument list and returns the values of the arguments as a <a href="https://docs.microsoft.com/windows/desktop/direct3dhlsl/printf">printf</a>-style formatted string.
            
            
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

A <a href="https://docs.microsoft.com/windows/desktop/direct3dhlsl/printf">printf</a>-style format string. The %s format identifier should never be used in an unbounded form. To avoid potential buffer overruns, always specify a size; for instance "%32s".


### -param arg4 [in]

Additional parameters that contain the data to be output.


## -returns



Type: <b>int</b>

Returns the number of characters written to the buffer, excluding any terminating <b>NULL</b> characters. A negative value is returned if an error occurs.




## -remarks



<b>Security Warning:  </b>Using this function incorrectly can compromise the security of your application. The copied string is not guaranteed to be null-terminated. Consider using one of the following alternatives. <a href="https://docs.microsoft.com/windows/desktop/api/strsafe/nf-strsafe-stringcbprintfa">StringCbPrintf</a>, <a href="https://docs.microsoft.com/windows/desktop/api/strsafe/nf-strsafe-stringcbprintfexa">StringCbPrintfEx</a>, <a href="https://docs.microsoft.com/windows/desktop/api/strsafe/nf-strsafe-stringcbvprintfa">StringCbVPrintf</a>, <a href="https://docs.microsoft.com/windows/desktop/api/strsafe/nf-strsafe-stringcbvprintfexa">StringCbVPrintfEx</a>, <a href="https://docs.microsoft.com/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa">StringCchPrintf</a>, <a href="https://docs.microsoft.com/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfexa">StringCchPrintfEx</a>, <a href="https://docs.microsoft.com/windows/desktop/api/strsafe/nf-strsafe-stringcchvprintfa">StringCchVPrintf</a>, or <a href="https://docs.microsoft.com/windows/desktop/api/strsafe/nf-strsafe-stringcchvprintfexa">StringCchVPrintfEx</a>. You should review <a href="https://docs.microsoft.com/windows/desktop/shell/sec-shell">Security Considerations: Microsoft Windows Shell</a> before continuing.

This is a Windows version of <a href="https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/ybk95axf(v=vs.100)">sprintf</a>. It does not support floating-point or pointer types. It supports only the left alignment flag.



