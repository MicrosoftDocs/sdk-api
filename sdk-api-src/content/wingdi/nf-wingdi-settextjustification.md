---
UID: NF:wingdi.SetTextJustification
title: SetTextJustification function (wingdi.h)
description: The SetTextJustification function specifies the amount of space the system should add to the break characters in a string of text. The space is added when an application calls the TextOut or ExtTextOut functions.
helpviewer_keywords: ["SetTextJustification","SetTextJustification function [Windows GDI]","_win32_SetTextJustification","gdi.settextjustification","wingdi/SetTextJustification"]
old-location: gdi\settextjustification.htm
tech.root: gdi
ms.assetid: 55fb5a28-b7da-40d8-8e64-4b42c23fa8b1
ms.date: 12/05/2018
ms.keywords: SetTextJustification, SetTextJustification function [Windows GDI], _win32_SetTextJustification, gdi.settextjustification, wingdi/SetTextJustification
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetTextJustification
 - wingdi/SetTextJustification
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - SetTextJustification
---

# SetTextJustification function


## -description

The <b>SetTextJustification</b> function specifies the amount of space the system should add to the break characters in a string of text. The space is added when an application calls the <a href="/windows/desktop/api/wingdi/nf-wingdi-textouta">TextOut</a> or <a href="/windows/desktop/api/wingdi/nf-wingdi-exttextouta">ExtTextOut</a> functions.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param extra [in]

The total extra space, in logical units, to be added to the line of text. If the current mapping mode is not MM_TEXT, the value identified by the <i>nBreakExtra</i> parameter is transformed and rounded to the nearest pixel.

### -param count [in]

The number of break characters in the line.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The break character is usually the space character (ASCII 32), but it may be defined by a font as some other character. The <a href="/windows/desktop/api/wingdi/nf-wingdi-gettextmetrics">GetTextMetrics</a> function can be used to retrieve a font's break character.

The <a href="/windows/desktop/api/wingdi/nf-wingdi-textouta">TextOut</a> function distributes the specified extra space evenly among the break characters in the line.

The <a href="/windows/desktop/api/wingdi/nf-wingdi-gettextextentpoint32a">GetTextExtentPoint32</a> function is always used with the <b>SetTextJustification</b> function. Sometimes the <b>GetTextExtentPoint32</b> function takes justification into account when computing the width of a specified line before justification, and sometimes it does not. For more details on this, see <b>GetTextExtentPoint32</b>. This width must be known before an appropriate <i>nBreakExtra</i> value can be computed.

<b>SetTextJustification</b> can be used to justify a line that contains multiple strings in different fonts. In this case, each string must be justified separately.

Because rounding errors can occur during justification, the system keeps a running error term that defines the current error value. When justifying a line that contains multiple runs, <a href="/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa">GetTextExtentPoint</a> automatically uses this error term when it computes the extent of the next run, allowing <a href="/windows/desktop/api/wingdi/nf-wingdi-textouta">TextOut</a> to blend the error into the new run. After each line has been justified, this error term must be cleared to prevent it from being incorporated into the next line. The term can be cleared by calling <b>SetTextJustification</b> with <i>nBreakExtra</i> set to zero.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-exttextouta">ExtTextOut</a>



<a href="/windows/desktop/gdi/font-and-text-functions">Font and Text Functions</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-gettextextentpoint32a">GetTextExtentPoint32</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-gettextmetrics">GetTextMetrics</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-textouta">TextOut</a>