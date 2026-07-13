---
UID: NF:winuser.GetTabbedTextExtentW
title: GetTabbedTextExtentW function (winuser.h)
description: The GetTabbedTextExtent function computes the width and height of a character string. (Unicode)
helpviewer_keywords: ["GetTabbedTextExtent", "GetTabbedTextExtent function [Windows GDI]", "GetTabbedTextExtentW", "_win32_GetTabbedTextExtent", "gdi.gettabbedtextextent", "winuser/GetTabbedTextExtent", "winuser/GetTabbedTextExtentW"]
old-location: gdi\gettabbedtextextent.htm
tech.root: gdi
ms.assetid: 3444bb8d-4a30-47d4-b211-01f7cba39975
ms.date: 12/05/2018
ms.keywords: GetTabbedTextExtent, GetTabbedTextExtent function [Windows GDI], GetTabbedTextExtentA, GetTabbedTextExtentW, _win32_GetTabbedTextExtent, gdi.gettabbedtextextent, winuser/GetTabbedTextExtent, winuser/GetTabbedTextExtentA, winuser/GetTabbedTextExtentW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetTabbedTextExtentW (Unicode) and GetTabbedTextExtentA (ANSI)
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
 - GetTabbedTextExtentW
 - winuser/GetTabbedTextExtentW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-misc-l1-7-0.dll
 - ext-ms-win-ntuser-misc-l1-6-0.dll
 - ext-ms-win-ntuser-misc-l1-5-1.dll
 - ext-ms-win-ntuser-misc-l1-5-0.dll
 - ext-ms-win-ntuser-misc-l1-3-0.dll
 - ext-ms-win-ntuser-misc-l1-2-0.dll
 - ext-ms-win-ntuser-misc-l1-1-0.dll
 - user32.dll
api_name:
 - GetTabbedTextExtent
 - GetTabbedTextExtentA
 - GetTabbedTextExtentW
---

# GetTabbedTextExtentW function


## -description

The <b>GetTabbedTextExtent</b> function computes the width and height of a character string. If the string contains one or more tab characters, the width of the string is based upon the specified tab stops. The <b>GetTabbedTextExtent</b> function uses the currently selected font to compute the dimensions of the string.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param lpString [in]

A pointer to a character string.

### -param chCount [in]

The length of the text string. For the ANSI function it is a BYTE count and for the Unicode function it is a WORD count. Note that for the ANSI function, characters in SBCS code pages take one byte each, while most characters in DBCS code pages take two bytes; for the Unicode function, most currently defined Unicode characters (those in the Basic Multilingual Plane (BMP)) are one WORD while Unicode surrogates are two WORDs.

### -param nTabPositions [in]

The number of tab-stop positions in the array pointed to by the <i>lpnTabStopPositions</i> parameter.

### -param lpnTabStopPositions [in]

A pointer to an array containing the tab-stop positions, in device units. The tab stops must be sorted in increasing order; the smallest x-value should be the first item in the array.

## -returns

If the function succeeds, the return value is the dimensions of the string in logical units. The height is in the high-order word and the width is in the low-order word.

If the function fails, the return value is 0. <b>GetTabbedTextExtent</b> will fail if <i>hDC</i> is invalid and if <i>nTabPositions</i> is less than 0.

## -remarks

The current clipping region does not affect the width and height returned by the <b>GetTabbedTextExtent</b> function.

Because some devices do not place characters in regular cell arrays (that is, they kern the characters), the sum of the extents of the characters in a string may not be equal to the extent of the string.

If the <i>nTabPositions</i> parameter is zero and the <i>lpnTabStopPositions</i> parameter is <b>NULL</b>, tabs are expanded to eight times the average character width.

If <i>nTabPositions</i> is 1, the tab stops are separated by the distance specified by the first value in the array to which <i>lpnTabStopPositions</i> points.





> [!NOTE]
> The winuser.h header defines GetTabbedTextExtent as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/gdi/font-and-text-functions">Font and Text Functions</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-gettextextentpoint32a">GetTextExtentPoint32</a>



<a href="/windows/desktop/api/winuser/nf-winuser-tabbedtextouta">TabbedTextOut</a>
