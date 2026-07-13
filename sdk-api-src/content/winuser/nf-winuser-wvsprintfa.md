---
UID: NF:winuser.wvsprintfA
title: wvsprintfA function (winuser.h)
description: Writes formatted data to the specified buffer using a pointer to a list of arguments. (ANSI)
helpviewer_keywords: ["winuser/wvsprintfA", "wvsprintfA"]
old-location: menurc\wvsprintf.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\wvsprintf.htm
ms.date: 12/05/2018
ms.keywords: _win32_wvsprintf, _win32_wvsprintf_cpp, menurc.wvsprintf, winui._win32_wvsprintf, winuser/wvsprintf, winuser/wvsprintfA, winuser/wvsprintfW, wvsprintf, wvsprintf function [Menus and Other Resources], wvsprintfA, wvsprintfW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: wvsprintfW (Unicode) and wvsprintfA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - wvsprintfA
 - winuser/wvsprintfA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - wvsprintf
 - wvsprintfA
 - wvsprintfW
---

# wvsprintfA function


## -description

Writes formatted data to the specified buffer using a pointer to a list of arguments. The items pointed to by the argument list are converted and copied to an output buffer according to the corresponding format specification in the format-control string. The function appends a terminating null character to the characters it writes, but the return value does not include the terminating null character in its character count.
<div class="alert"><b>Warning</b>  Do not use. Consider using one of the following functions instead: <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbvprintfa">StringCbVPrintf</a>, 
				<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbvprintfexa">StringCbVPrintfEx</a>, <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchvprintfa">StringCchVPrintf</a>, or
				<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchvprintfexa">StringCchVPrintfEx</a>. See Security Considerations.</div><div> </div>

## -parameters

### -param unnamedParam1 [out]

Type: <b>LPTSTR</b>

The buffer that is to receive the formatted output. The maximum size of the buffer is 1,024 bytes.

### -param unnamedParam2 [in]

Type: <b>LPCTSTR</b>

The format-control specifications. In addition to ordinary ASCII characters, a format specification for each argument appears in this string. For more information about the format specification, see the <a href="/windows/desktop/api/winuser/nf-winuser-wsprintfa">wsprintf</a> function.

### -param arglist [in]

Type: <b>va_list</b>

Each element of this list specifies an argument for the format-control string. The number, type, and interpretation of the arguments depend on the corresponding format-control specifications in the 
					<i>lpFmt</i> parameter.

## -returns

Type: <b>int</b>

If the function succeeds, the return value is the number of characters stored in the buffer, not counting the terminating null character.

If the function fails, the return value is less than the length of the expected output. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The function copies the format-control string into the output buffer character by character, starting with the first character in the string. When it encounters a format specification in the string, the function retrieves the value of the next available argument (starting with the first argument in the list), converts that value into the specified format, and copies the result to the output buffer. The function continues to copy characters and expand format specifications in this way until it reaches the end of the format-control string. If there are more arguments than format specifications, the extra arguments are ignored. If there are not enough arguments for all of the format specifications, the results are undefined.





> [!NOTE]
> The winuser.h header defines wvsprintf as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<b>Reference</b>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbprintfa">StringCbPrintf</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbprintfexa">StringCbPrintfEx</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbvprintfa">StringCbVPrintf</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbvprintfexa">StringCbVPrintfEx</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa">StringCchPrintf</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfexa">StringCchPrintfEx</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchvprintfa">StringCchVPrintf</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchvprintfexa">StringCchVPrintfEx</a>



<a href="/windows/desktop/menurc/strings">Strings</a>



<a href="/windows/desktop/api/winuser/nf-winuser-wsprintfa">wsprintf</a>
