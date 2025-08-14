---
UID: NF:uxtheme.DrawThemeTextEx
title: DrawThemeTextEx function (uxtheme.h)
description: Draws text using the color and font defined by the visual style. Extends DrawThemeText by allowing additional text format options.
helpviewer_keywords: ["DrawThemeTextEx","DrawThemeTextEx function [Windows Controls]","controls.DrawThemeTextEx","controls.inet_DrawThemeTextEx","inet_DrawThemeTextEx","inet_DrawThemeTextEx_cpp","uxtheme/DrawThemeTextEx"]
old-location: controls\DrawThemeTextEx.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\drawthemetextex.htm
ms.date: 12/05/2018
ms.keywords: DrawThemeTextEx, DrawThemeTextEx function [Windows Controls], controls.DrawThemeTextEx, controls.inet_DrawThemeTextEx, inet_DrawThemeTextEx, inet_DrawThemeTextEx_cpp, uxtheme/DrawThemeTextEx
req.header: uxtheme.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: UxTheme.lib
req.dll: UxTheme.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DrawThemeTextEx
 - uxtheme/DrawThemeTextEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-uxtheme-themes-l1-1-3.dll
 - ext-ms-win-uxtheme-themes-l1-1-2.dll
 - UxTheme.dll
 - ext-ms-win-uxtheme-themes-l1-1-1.dll
 - xamlpalwp.dll
api_name:
 - DrawThemeTextEx
---

# DrawThemeTextEx function


## -description

Draws text using the color and font defined by the visual style. Extends <a href="/windows/desktop/api/uxtheme/nf-uxtheme-drawthemetext">DrawThemeText</a> by allowing additional text format options.

## -parameters

### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to a window's specified theme data. Use <a href="/windows/desktop/api/uxtheme/nf-uxtheme-openthemedata">OpenThemeData</a> to create an HTHEME.

### -param hdc [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HDC</a></b>

HDC to use for drawing.

### -param iPartId [in]

Type: <b>int</b>

The control part that has the desired text appearance. See <a href="/windows/desktop/Controls/parts-and-states">Parts and States</a>. If this value is 0, the text is drawn in the default font, or a font selected into the device context.

### -param iStateId [in]

Type: <b>int</b>

The control state that has the desired text appearance. See <a href="/windows/desktop/Controls/parts-and-states">Parts and States</a>.

### -param pszText [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCWSTR</a></b>

Pointer to a string that contains the text to draw.

### -param cchText [in]

Type: <b>int</b>

Value of type <b>int</b> that contains the number of characters to draw. If the parameter is set to -1, all the characters in the string are drawn.

### -param dwTextFlags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

<b>DWORD</b> that contains one or more values that specify the string's formatting. See <a href="/windows/desktop/Controls/theme-format-values">Format Values</a> for possible parameter values.

### -param pRect [in, out]

Type: <b>LPRECT</b>

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that contains the rectangle, in logical coordinates, in which the text is to be drawn.

### -param pOptions [in]

Type: <b>const <a href="/windows/desktop/api/uxtheme/ns-uxtheme-dttopts">DTTOPTS</a>*</b>

A <a href="/windows/desktop/api/uxtheme/ns-uxtheme-dttopts">DTTOPTS</a> structure that defines additional formatting options that will be applied to the text being drawn.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The function always uses the themed font for the specified part and state if one is defined. Otherwise it uses the font currently selected into the device context. To find out if a themed font is defined, you can call <a href="/windows/desktop/api/uxtheme/nf-uxtheme-getthemefont">GetThemeFont</a> or <a href="/windows/desktop/api/uxtheme/nf-uxtheme-getthemepropertyorigin">GetThemePropertyOrigin</a> with TMT_FONT as the property identifier.