---
UID: NF:winuser.TabbedTextOutA
title: TabbedTextOutA function (winuser.h)
description: The TabbedTextOut function writes a character string at a specified location, expanding tabs to the values specified in an array of tab-stop positions. Text is written in the currently selected font, background color, and text color. (ANSI)
helpviewer_keywords: ["TabbedTextOutA", "winuser/TabbedTextOutA"]
old-location: gdi\tabbedtextout.htm
tech.root: gdi
ms.assetid: 1cb78a75-752d-4e06-afdf-cd797f209114
ms.date: 12/05/2018
ms.keywords: TabbedTextOut, TabbedTextOut function [Windows GDI], TabbedTextOutA, TabbedTextOutW, _win32_TabbedTextOut, gdi.tabbedtextout, winuser/TabbedTextOut, winuser/TabbedTextOutA, winuser/TabbedTextOutW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: TabbedTextOutW (Unicode) and TabbedTextOutA (ANSI)
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
 - TabbedTextOutA
 - winuser/TabbedTextOutA
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
 - user32.dll
 - Ext-MS-Win-NTUser-Misc-l1-1-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-2-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-3-0.dll
 - ext-ms-win-ntuser-misc-l1-3-1.dll
 - Ext-MS-Win-NTUser-Misc-L1-4-0.dll
 - Ext-Ms-Win-NTUser-Misc-L1-5-0.dll
 - Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
 - TabbedTextOut
 - TabbedTextOutA
 - TabbedTextOutW
req.apiset: ext-ms-win-ntuser-misc-l1-5-1 (introduced in Windows 10, version 10.0.14393)
---

# TabbedTextOutA function


## -description

The <b>TabbedTextOut</b> function writes a character string at a specified location, expanding tabs to the values specified in an array of tab-stop positions. Text is written in the currently selected font, background color, and text color.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param x [in]

The x-coordinate of the starting point of the string, in logical units.

### -param y [in]

The y-coordinate of the starting point of the string, in logical units.

### -param lpString [in]

A pointer to the character string to draw. The string does not need to be zero-terminated, since <i>nCount</i> specifies the length of the string.

### -param chCount [in]

The <a href="/windows/desktop/gdi/specifying-length-of-text-output-string">length of the string</a> pointed to by <i>lpString</i>.

### -param nTabPositions [in]

The number of values in the array of tab-stop positions.

### -param lpnTabStopPositions [in]

A pointer to an array containing the tab-stop positions, in logical units. The tab stops must be sorted in increasing order; the smallest x-value should be the first item in the array.

### -param nTabOrigin [in]

The x-coordinate of the starting position from which tabs are expanded, in logical units.

## -returns

If the function succeeds, the return value is the dimensions, in logical units, of the string. The height is in the high-order word and the width is in the low-order word.

If the function fails, the return value is zero.

## -remarks

If the <i>nTabPositions</i> parameter is zero and the <i>lpnTabStopPositions</i> parameter is <b>NULL</b>, tabs are expanded to eight times the average character width.

If <i>nTabPositions</i> is 1, the tab stops are separated by the distance specified by the first value in the <i>lpnTabStopPositions</i> array.

If the <i>lpnTabStopPositions</i> array contains more than one value, a tab stop is set for each value in the array, up to the number specified by <i>nTabPositions</i>.

The <i>nTabOrigin</i> parameter allows an application to call the <b>TabbedTextOut</b> function several times for a single line. If the application calls <b>TabbedTextOut</b> more than once with the <i>nTabOrigin</i> set to the same value each time, the function expands all tabs relative to the position specified by <i>nTabOrigin</i>.

By default, the current position is not used or updated by the <b>TabbedTextOut</b> function. If an application needs to update the current position when it calls <b>TabbedTextOut</b>, the application can call the <a href="/windows/desktop/api/wingdi/nf-wingdi-settextalign">SetTextAlign</a> function with the <i>wFlags</i> parameter set to TA_UPDATECP. When this flag is set, the system ignores the <i>X</i> and <i>Y</i> parameters on subsequent calls to the <b>TabbedTextOut</b> function, using the current position instead.

<div class="alert"><b>Note</b>  For Windows Vista and later, <b>TabbedTextOut</b> ignores text alignment when it draws text. </div>
<div> </div>




> [!NOTE]
> The winuser.h header defines TabbedTextOut as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-drawtext">DrawText</a>



<a href="/windows/desktop/gdi/font-and-text-functions">Font and Text Functions</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/winuser/nf-winuser-gettabbedtextextenta">GetTabbedTextExtent</a>



<a href="/windows/desktop/api/winuser/nf-winuser-graystringa">GrayString</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-selectobject">SelectObject</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setbkcolor">SetBkColor</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-settextalign">SetTextAlign</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-settextcolor">SetTextColor</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-textouta">TextOut</a>
