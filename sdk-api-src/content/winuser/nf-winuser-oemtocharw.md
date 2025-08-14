---
UID: NF:winuser.OemToCharW
title: OemToCharW function (winuser.h)
description: Translates a string from the OEM-defined character set into either an ANSI or a wide-character string.Warning  Do not use. (Unicode)
helpviewer_keywords: ["OemToChar", "OemToChar function [Menus and Other Resources]", "OemToCharW", "_win32_OemToChar", "_win32_oemtochar_cpp", "menurc.oemtochar", "winui._win32_oemtochar", "winuser/OemToChar", "winuser/OemToCharW"]
old-location: menurc\oemtochar.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\oemtochar.htm
ms.date: 07/10/2025
ms.keywords: OemToChar, OemToChar function [Menus and Other Resources], OemToCharA, OemToCharW, _win32_OemToChar, _win32_oemtochar_cpp, menurc.oemtochar, winui._win32_oemtochar, winuser/OemToChar, winuser/OemToCharA, winuser/OemToCharW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OemToCharW (Unicode) and OemToCharA (ANSI)
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
 - OemToCharW
 - winuser/OemToCharW
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
 - OemToChar
 - OemToCharA
 - OemToCharW
req.apiset: ext-ms-win-ntuser-chartranslation-l1-1-0 (introduced in Windows 8)
---

# OemToCharW function


## -description

Translates a string from the OEM-defined character set into either an ANSI or a wide-character string.
<div class="alert"><b>Warning</b>  Do not use. See Security Considerations.</div><div> </div>

## -parameters

### -param pSrc [in]

Type: <b>LPCSTR</b>

A null-terminated string of characters from the OEM-defined character set.

### -param pDst [out]

Type: <b>LPTSTR</b>

The destination buffer, which receives the translated string. If the <b>OemToChar</b> function is being used as an ANSI function, the string can be translated in place by setting the <i>lpszDst</i> parameter to the same address as the <i>lpszSrc</i> parameter. This cannot be done if <b>OemToChar</b> is being used as a wide-character function.

## -returns

Type: <b>BOOL</b>

The return value is always nonzero except when you pass the same address to <i>lpszSrc</i> and <i>lpszDst</i> in the wide-character version of the function. In this case the function returns zero and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns <b>ERROR_INVALID_ADDRESS</b>.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-chartooema">CharToOem</a>

<a href="/windows/desktop/api/winuser/nf-winuser-chartooembuffa">CharToOemBuff</a>

<b>Conceptual</b>

<a href="/windows/desktop/api/winuser/nf-winuser-oemtocharbuffa">OemToCharBuff</a>

<b>Reference</b>

<a href="/windows/desktop/menurc/strings">Strings</a>

## -remarks

### Security Considerations

Using this function incorrectly might compromise the security of your program. For example, miscalculating the proper size of the *lpszDst* buffer, especially when the application is used in both ANSI and Unicode versions, can cause a buffer overflow. For more information, see [Security Considerations: International Features](/windows/desktop/Intl/security-considerations--international-features) and [Security Considerations: Windows User Interface](/windows/win32/appuistart/sec-ui).

> [!NOTE]
> The winuser.h header defines OemToChar as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
