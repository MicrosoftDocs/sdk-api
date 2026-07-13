---
UID: NF:winuser.OemToCharBuffW
title: OemToCharBuffW function (winuser.h)
description: Translates a specified number of characters in a string from the OEM-defined character set into either an ANSI or a wide-character string. (Unicode)
helpviewer_keywords: ["OemToCharBuff", "OemToCharBuff function [Menus and Other Resources]", "OemToCharBuffW", "_win32_OemToCharBuff", "_win32_oemtocharbuff_cpp", "menurc.oemtocharbuff", "winui._win32_oemtocharbuff", "winuser/OemToCharBuff", "winuser/OemToCharBuffW"]
old-location: menurc\oemtocharbuff.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\oemtocharbuff.htm
ms.date: 12/05/2018
ms.keywords: OemToCharBuff, OemToCharBuff function [Menus and Other Resources], OemToCharBuffA, OemToCharBuffW, _win32_OemToCharBuff, _win32_oemtocharbuff_cpp, menurc.oemtocharbuff, winui._win32_oemtocharbuff, winuser/OemToCharBuff, winuser/OemToCharBuffA, winuser/OemToCharBuffW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OemToCharBuffW (Unicode) and OemToCharBuffA (ANSI)
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
 - OemToCharBuffW
 - winuser/OemToCharBuffW
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
 - OemToCharBuff
 - OemToCharBuffA
 - OemToCharBuffW
req.apiset: ext-ms-win-ntuser-chartranslation-l1-1-0 (introduced in Windows 8)
---

# OemToCharBuffW function


## -description

Translates a specified number of characters in a string from the OEM-defined character set into either an ANSI or a wide-character string.

## -parameters

### -param lpszSrc [in]

Type: <b>LPCSTR</b>

One or more characters from the OEM-defined character set.

### -param lpszDst [out]

Type: <b>LPTSTR</b>

The destination buffer, which receives the translated string. If the <b>OemToCharBuff</b> function is being used as an ANSI function, the string can be translated in place by setting the 
					<i>lpszDst</i> parameter to the same address as the 
					<i>lpszSrc</i> parameter. This cannot be done if the <b>OemToCharBuff</b> function is being used as a wide-character function.

### -param cchDstLength [in]

Type: <b>DWORD</b>

The number of 
					characters to be translated in the buffer identified by the 
					<i>lpszSrc</i> parameter.

## -returns

Type: <b>BOOL</b>

The return value is always nonzero except when you pass the same address to 
						<i>lpszSrc</i> and 
						<i>lpszDst</i> in the wide-character version of the function. In this case the function returns zero and 
						<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns <b>ERROR_INVALID_ADDRESS</b>.

## -remarks

Unlike the <a href="/windows/desktop/api/winuser/nf-winuser-oemtochara">OemToChar</a> function, the <b>OemToCharBuff</b> function does not stop converting characters when it encounters a null character in the buffer pointed to by 
				<i>lpszSrc</i>. The <b>OemToCharBuff</b> function converts all 
				<i>cchDstLength</i> characters.





> [!NOTE]
> The winuser.h header defines OemToCharBuff as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-chartooema">CharToOem</a>



<a href="/windows/desktop/api/winuser/nf-winuser-chartooembuffa">CharToOemBuff</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-oemtochara">OemToChar</a>



<b>Reference</b>



<a href="/windows/desktop/menurc/strings">Strings</a>
