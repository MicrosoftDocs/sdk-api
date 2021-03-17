---
UID: NF:uxtheme.GetThemeSysColorBrush
title: GetThemeSysColorBrush function (uxtheme.h)
description: Retrieves a system color brush.
helpviewer_keywords: ["GetThemeSysColorBrush","GetThemeSysColorBrush function [Windows Controls]","TMT_ACTIVEBORDER","TMT_ACTIVECAPTION","TMT_APPWORKSPACE","TMT_BACKGROUND","TMT_BTNFACE","TMT_BTNHIGHLIGHT","TMT_BTNSHADOW","TMT_BTNTEXT","TMT_BUTTONALTERNATEFACE","TMT_CAPTIONTEXT","TMT_DKSHADOW3D","TMT_GRADIENTACTIVECAPTION","TMT_GRADIENTINACTIVECAPTION","TMT_GRAYTEXT","TMT_HIGHLIGHT","TMT_HIGHLIGHTTEXT","TMT_HOTTRACKING","TMT_INACTIVEBORDER","TMT_INACTIVECAPTION","TMT_INACTIVECAPTIONTEXT","TMT_INFOBK","TMT_INFOTEXT","TMT_LIGHT3D","TMT_MENUBAR","TMT_MENUHILIGHT","TMT_MENUTEXT","TMT_SCROLLBAR","TMT_WINDOW","TMT_WINDOWFRAME","TMT_WINDOWTEXT","controls.GetThemeSysColorBrush","controls.inet_GetThemeSysColorBrush","inet_GetThemeSysColorBrush","inet_GetThemeSysColorBrush_cpp","uxtheme/GetThemeSysColorBrush"]
old-location: controls\GetThemeSysColorBrush.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\getthemesyscolorbrush.htm
ms.date: 12/05/2018
ms.keywords: GetThemeSysColorBrush, GetThemeSysColorBrush function [Windows Controls], TMT_ACTIVEBORDER, TMT_ACTIVECAPTION, TMT_APPWORKSPACE, TMT_BACKGROUND, TMT_BTNFACE, TMT_BTNHIGHLIGHT, TMT_BTNSHADOW, TMT_BTNTEXT, TMT_BUTTONALTERNATEFACE, TMT_CAPTIONTEXT, TMT_DKSHADOW3D, TMT_GRADIENTACTIVECAPTION, TMT_GRADIENTINACTIVECAPTION, TMT_GRAYTEXT, TMT_HIGHLIGHT, TMT_HIGHLIGHTTEXT, TMT_HOTTRACKING, TMT_INACTIVEBORDER, TMT_INACTIVECAPTION, TMT_INACTIVECAPTIONTEXT, TMT_INFOBK, TMT_INFOTEXT, TMT_LIGHT3D, TMT_MENUBAR, TMT_MENUHILIGHT, TMT_MENUTEXT, TMT_SCROLLBAR, TMT_WINDOW, TMT_WINDOWFRAME, TMT_WINDOWTEXT, controls.GetThemeSysColorBrush, controls.inet_GetThemeSysColorBrush, inet_GetThemeSysColorBrush, inet_GetThemeSysColorBrush_cpp, uxtheme/GetThemeSysColorBrush
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
 - GetThemeSysColorBrush
 - uxtheme/GetThemeSysColorBrush
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
 - GetThemeSysColorBrush
---

# GetThemeSysColorBrush function


## -description

Retrieves a system color brush.

## -parameters

### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to theme data.

### -param iColorId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the number of the desired system color.  May be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TMT_SCROLLBAR"></a><a id="tmt_scrollbar"></a><dl>
<dt><b>TMT_SCROLLBAR</b></dt>
</dl>
</td>
<td width="60%">
The color of scroll bars.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_BACKGROUND"></a><a id="tmt_background"></a><dl>
<dt><b>TMT_BACKGROUND</b></dt>
</dl>
</td>
<td width="60%">
The color of the background.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_ACTIVECAPTION"></a><a id="tmt_activecaption"></a><dl>
<dt><b>TMT_ACTIVECAPTION</b></dt>
</dl>
</td>
<td width="60%">
The color of the caption area on an active window.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_INACTIVECAPTION"></a><a id="tmt_inactivecaption"></a><dl>
<dt><b>TMT_INACTIVECAPTION</b></dt>
</dl>
</td>
<td width="60%">
The color of the caption area on an inactive window.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_WINDOW"></a><a id="tmt_window"></a><dl>
<dt><b>TMT_WINDOW</b></dt>
</dl>
</td>
<td width="60%">
The color of a window.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_WINDOWFRAME"></a><a id="tmt_windowframe"></a><dl>
<dt><b>TMT_WINDOWFRAME</b></dt>
</dl>
</td>
<td width="60%">
The color of the frame around a window.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_MENUTEXT"></a><a id="tmt_menutext"></a><dl>
<dt><b>TMT_MENUTEXT</b></dt>
</dl>
</td>
<td width="60%">
The color of text drawn on a menu.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_WINDOWTEXT"></a><a id="tmt_windowtext"></a><dl>
<dt><b>TMT_WINDOWTEXT</b></dt>
</dl>
</td>
<td width="60%">
The color of text drawn in a window.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_CAPTIONTEXT"></a><a id="tmt_captiontext"></a><dl>
<dt><b>TMT_CAPTIONTEXT</b></dt>
</dl>
</td>
<td width="60%">
The color of text drawn in the caption area of an active window.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_ACTIVEBORDER"></a><a id="tmt_activeborder"></a><dl>
<dt><b>TMT_ACTIVEBORDER</b></dt>
</dl>
</td>
<td width="60%">
The color of the border around an active window.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_INACTIVEBORDER"></a><a id="tmt_inactiveborder"></a><dl>
<dt><b>TMT_INACTIVEBORDER</b></dt>
</dl>
</td>
<td width="60%">
The color of the border around an inactive window.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_APPWORKSPACE"></a><a id="tmt_appworkspace"></a><dl>
<dt><b>TMT_APPWORKSPACE</b></dt>
</dl>
</td>
<td width="60%">
The color of the application workspace.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_HIGHLIGHT"></a><a id="tmt_highlight"></a><dl>
<dt><b>TMT_HIGHLIGHT</b></dt>
</dl>
</td>
<td width="60%">
The color of a highlight.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_HIGHLIGHTTEXT"></a><a id="tmt_highlighttext"></a><dl>
<dt><b>TMT_HIGHLIGHTTEXT</b></dt>
</dl>
</td>
<td width="60%">
The color of highlighted text.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_BTNFACE"></a><a id="tmt_btnface"></a><dl>
<dt><b>TMT_BTNFACE</b></dt>
</dl>
</td>
<td width="60%">
The color of a button face.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_BTNSHADOW"></a><a id="tmt_btnshadow"></a><dl>
<dt><b>TMT_BTNSHADOW</b></dt>
</dl>
</td>
<td width="60%">
The color of the shadow underneath a button.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_GRAYTEXT"></a><a id="tmt_graytext"></a><dl>
<dt><b>TMT_GRAYTEXT</b></dt>
</dl>
</td>
<td width="60%">
The color of dimmed text.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_BTNTEXT"></a><a id="tmt_btntext"></a><dl>
<dt><b>TMT_BTNTEXT</b></dt>
</dl>
</td>
<td width="60%">
The color of text contained within a button.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_INACTIVECAPTIONTEXT"></a><a id="tmt_inactivecaptiontext"></a><dl>
<dt><b>TMT_INACTIVECAPTIONTEXT</b></dt>
</dl>
</td>
<td width="60%">
The color of the text in the caption area of an inactive window.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_BTNHIGHLIGHT"></a><a id="tmt_btnhighlight"></a><dl>
<dt><b>TMT_BTNHIGHLIGHT</b></dt>
</dl>
</td>
<td width="60%">
The color of the highlight around a button.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_DKSHADOW3D"></a><a id="tmt_dkshadow3d"></a><dl>
<dt><b>TMT_DKSHADOW3D</b></dt>
</dl>
</td>
<td width="60%">
The color of three-dimensional dark shadows.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_LIGHT3D"></a><a id="tmt_light3d"></a><dl>
<dt><b>TMT_LIGHT3D</b></dt>
</dl>
</td>
<td width="60%">
The color of three-dimensional light areas.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_INFOTEXT"></a><a id="tmt_infotext"></a><dl>
<dt><b>TMT_INFOTEXT</b></dt>
</dl>
</td>
<td width="60%">
The color of informational text.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_INFOBK"></a><a id="tmt_infobk"></a><dl>
<dt><b>TMT_INFOBK</b></dt>
</dl>
</td>
<td width="60%">
The color of the background behind informational text.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_BUTTONALTERNATEFACE"></a><a id="tmt_buttonalternateface"></a><dl>
<dt><b>TMT_BUTTONALTERNATEFACE</b></dt>
</dl>
</td>
<td width="60%">
The color of the alternate face of a button.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_HOTTRACKING"></a><a id="tmt_hottracking"></a><dl>
<dt><b>TMT_HOTTRACKING</b></dt>
</dl>
</td>
<td width="60%">
The color of highlight applied when a user moves the mouse over a control.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_GRADIENTACTIVECAPTION"></a><a id="tmt_gradientactivecaption"></a><dl>
<dt><b>TMT_GRADIENTACTIVECAPTION</b></dt>
</dl>
</td>
<td width="60%">
The gradient color applied to the caption area of an active window.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_GRADIENTINACTIVECAPTION"></a><a id="tmt_gradientinactivecaption"></a><dl>
<dt><b>TMT_GRADIENTINACTIVECAPTION</b></dt>
</dl>
</td>
<td width="60%">
The gradient color applied to the caption area of an inactive window.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_MENUHILIGHT"></a><a id="tmt_menuhilight"></a><dl>
<dt><b>TMT_MENUHILIGHT</b></dt>
</dl>
</td>
<td width="60%">
The color of highlight drawn on a menu item when the user moves the mouse over it.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_MENUBAR"></a><a id="tmt_menubar"></a><dl>
<dt><b>TMT_MENUBAR</b></dt>
</dl>
</td>
<td width="60%">
The color of the menu bar.

</td>
</tr>
</table>

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HBRUSH</a></b>

Handle to brush data.

## -remarks

If the theme data handle is not a <b>NULL</b> handle, <b>GetThemeSysColorBrush</b> returns the brush that matches the specified color from the SysMetrics section of the visual style. If the theme data handle is <b>NULL</b>, the function returns the brush matching the global system color.


The brush handle that is returned by this function should be released when it is no longer needed using <a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a>.