---
UID: NF:uxtheme.GetThemeTextExtent
title: GetThemeTextExtent function (uxtheme.h)
description: Calculates the size and location of the specified text when rendered in the visual style font.
helpviewer_keywords: ["GetThemeTextExtent","GetThemeTextExtent function [Windows Controls]","controls.GetThemeTextExtent","controls.inet_GetThemeTextExtent","inet_GetThemeTextExtent","inet_GetThemeTextExtent_cpp","uxtheme/GetThemeTextExtent"]
old-location: controls\GetThemeTextExtent.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\getthemetextextent.htm
ms.date: 12/05/2018
ms.keywords: GetThemeTextExtent, GetThemeTextExtent function [Windows Controls], controls.GetThemeTextExtent, controls.inet_GetThemeTextExtent, inet_GetThemeTextExtent, inet_GetThemeTextExtent_cpp, uxtheme/GetThemeTextExtent
req.header: uxtheme.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - GetThemeTextExtent
 - uxtheme/GetThemeTextExtent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - UxTheme.dll
api_name:
 - GetThemeTextExtent
---

# GetThemeTextExtent function


## -description

Calculates the size and location of the specified text when rendered in the visual style font.

## -parameters

### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to a window's specified theme data. Use <a href="/windows/desktop/api/uxtheme/nf-uxtheme-openthemedata">OpenThemeData</a> to create an HTHEME.

### -param hdc [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HDC</a></b>

HDC to select the font into.

### -param iPartId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the part in which the text will be drawn. See <a href="/windows/desktop/Controls/parts-and-states">Parts and States</a>.

### -param iStateId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the state of the part. See <a href="/windows/desktop/Controls/parts-and-states">Parts and States</a>.

### -param pszText [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCWSTR</a></b>

Pointer to a string that contains the text to draw.

### -param cchCharCount [in]

Type: <b>int</b>

Value of type <b>int</b> that contains the number of characters to draw. If the parameter is set to -1, all the characters in the string are drawn.

### -param dwTextFlags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

<b>DWORD</b> that contains one or more values that specify the string's formatting. See <a href="/windows/desktop/Controls/theme-format-values">Format Values</a> for possible parameter values.

### -param pBoundingRect [in]

Type: <b>LPCRECT</b>

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that contains the rectangle used to control layout of the text. This parameter may be set to <b>NULL</b>.

### -param pExtentRect [out]

Type: <b>LPRECT</b>

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that contains, in logical coordinates, the rectangle required to fit the rendered text.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/Controls/property-typedefs">Property Identifiers</a>