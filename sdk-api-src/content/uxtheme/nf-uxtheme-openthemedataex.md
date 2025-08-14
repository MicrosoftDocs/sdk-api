---
UID: NF:uxtheme.OpenThemeDataEx
title: OpenThemeDataEx function (uxtheme.h)
description: Opens the theme data associated with a window for specified theme classes.
helpviewer_keywords: ["OTD_FORCE_RECT_SIZING","OTD_NONCLIENT","OpenThemeDataEx","OpenThemeDataEx function [Windows Controls]","controls.OpenThemeDataEx","controls.inet_OpenThemeDataEx","inet_OpenThemeDataEx","inet_OpenThemeDataEx_cpp","uxtheme/OpenThemeDataEx"]
old-location: controls\OpenThemeDataEx.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\openthemedataex.htm
ms.date: 12/05/2018
ms.keywords: OTD_FORCE_RECT_SIZING, OTD_NONCLIENT, OpenThemeDataEx, OpenThemeDataEx function [Windows Controls], controls.OpenThemeDataEx, controls.inet_OpenThemeDataEx, inet_OpenThemeDataEx, inet_OpenThemeDataEx_cpp, uxtheme/OpenThemeDataEx
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
 - OpenThemeDataEx
 - uxtheme/OpenThemeDataEx
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
 - Ext-MS-Win-UXTheme-Themes-l1-1-0.dll
 - xamlpalwp.dll
 - ext-ms-win-uxtheme-themes-l1-1-1.dll
api_name:
 - OpenThemeDataEx
---

# OpenThemeDataEx function


## -description

Opens the theme data associated with a window for specified theme classes.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to a window or control that the theme is to be retrieved from.

### -param pszClassList [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCWSTR</a></b>

A semicolon-separated list of class names to match.

### -param dwFlags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Optional flags that control how to return the theme data. May be set to a combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="OTD_FORCE_RECT_SIZING"></a><a id="otd_force_rect_sizing"></a><dl>
<dt><b>OTD_FORCE_RECT_SIZING</b></dt>
</dl>
</td>
<td width="60%">
Forces drawn images from this theme to stretch to fit the rectangles specified by drawing functions.

</td>
</tr>
<tr>
<td width="40%"><a id="OTD_NONCLIENT"></a><a id="otd_nonclient"></a><dl>
<dt><b>OTD_NONCLIENT</b></dt>
</dl>
</td>
<td width="60%">
Allows theme elements to be drawn in the non-client area of the window.

</td>
</tr>
</table>

## -returns

Type: <b>HTHEME</b>

If a match is found, a valid handle to a theme is returned. Otherwise, a <b>NULL</b> value will be returned.

## -remarks

The string specified by <i>pszClassIdList</i> will be tokenized using semicolons as a delimiter. The names are matched against class names one token at a time. If no match is found for a particular token, the next token will be matched. If a match is found, the return value of the function will be the theme handle associated with the matched class.

Class names for the Aero theme are defined in AeroStyle.xml.

## -see-also

<a href="/windows/desktop/api/uxtheme/nf-uxtheme-openthemedata">OpenThemeData</a>