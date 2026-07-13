---
UID: NF:winuser.CharLowerW
title: CharLowerW function (winuser.h)
description: Converts a character string or a single character to lowercase. If the operand is a character string, the function converts the characters in place. (Unicode)
helpviewer_keywords: ["CharLower", "CharLower function [Menus and Other Resources]", "CharLowerW", "_win32_CharLower", "_win32_charlower_cpp", "menurc.charlower", "winui._win32_charlower", "winuser/CharLower", "winuser/CharLowerW"]
old-location: menurc\charlower.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\charlower.htm
ms.date: 12/05/2018
ms.keywords: CharLower, CharLower function [Menus and Other Resources], CharLowerA, CharLowerW, _win32_CharLower, _win32_charlower_cpp, menurc.charlower, winui._win32_charlower, winuser/CharLower, winuser/CharLowerA, winuser/CharLowerW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CharLowerW (Unicode) and CharLowerA (ANSI)
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
 - CharLowerW
 - winuser/CharLowerW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - API-MS-Win-Core-String-l2-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-String-l2-1-1.dll
 - API-MS-Win-Core-Stringansi-l1-1-0.dll
 - API-MS-Win-deprecated-apis-Obsolete-l1-1-0.dll
 - API-MS-Win-DownLevel-user32-l1-1-0.dll
 - API-MS-Win-DownLevel-user32-l1-1-1.dll
api_name:
 - CharLower
 - CharLowerA
 - CharLowerW
---

# CharLowerW function


## -description

Converts a character string or a single character to lowercase. If the operand is a character string, the function converts the characters in place.

## -parameters

### -param lpsz [in, out]

Type: <b>LPTSTR</b>

A null-terminated string, or specifies a single character. If the high-order word of this parameter is zero, the low-order word must contain a single character to be converted.

## -returns

Type: <b>LPTSTR</b>

If the operand is a character string, the function returns a pointer to the converted string. Because the string is converted in place, the return value is equal to 
						<i>lpsz</i>. 

If the operand is a single character, the return value is a 32-bit value whose high-order word is zero, and low-order word contains the converted character. 

There is no indication of success or failure. Failure is rare. There is no extended error information for this function; do not call 
						<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Note that <b>CharLower</b> always maps uppercase I to lowercase I ("i"), even when the current language is Turkish or Azerbaijani. If you need a function that is linguistically sensitive in this respect, call <a href="/windows/desktop/api/winnls/nf-winnls-lcmapstringa">LCMapString</a>.

Conversion to Unicode in the ANSI version of the function is done with the system default locale in all cases.





> [!NOTE]
> The winuser.h header defines CharLower as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-charlowerbuffa">CharLowerBuff</a>



<a href="/windows/desktop/api/winuser/nf-winuser-charuppera">CharUpper</a>



<a href="/windows/desktop/api/winuser/nf-winuser-charupperbuffa">CharUpperBuff</a>



<b>Conceptual</b>



<b>Reference</b>



<a href="/windows/desktop/menurc/strings">Strings</a>
