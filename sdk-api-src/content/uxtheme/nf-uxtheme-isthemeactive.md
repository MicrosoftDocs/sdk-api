---
UID: NF:uxtheme.IsThemeActive
title: IsThemeActive function (uxtheme.h)
description: Tests if a visual style for the current application is active.
helpviewer_keywords: ["IsThemeActive","IsThemeActive function [Windows Controls]","controls.IsThemeActive","controls.inet_IsThemeActive","inet_IsThemeActive","inet_IsThemeActive_cpp","uxtheme/IsThemeActive"]
old-location: controls\IsThemeActive.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\isthemeactive.htm
ms.date: 12/05/2018
ms.keywords: IsThemeActive, IsThemeActive function [Windows Controls], controls.IsThemeActive, controls.inet_IsThemeActive, inet_IsThemeActive, inet_IsThemeActive_cpp, uxtheme/IsThemeActive
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
 - IsThemeActive
 - uxtheme/IsThemeActive
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
 - IsThemeActive
---

# IsThemeActive function


## -description

Tests if a visual style for the current application is active.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
A visual style is enabled, and windows with visual styles applied should call <a href="/windows/desktop/api/uxtheme/nf-uxtheme-openthemedata">OpenThemeData</a> to start using theme drawing services.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
A visual style is not enabled, and the window message handler does not need to make another call to <a href="/windows/desktop/api/uxtheme/nf-uxtheme-isthemeactive">IsThemeActive</a> until it receives a WM_THEMECHANGED message.

</td>
</tr>
</table>

## -remarks

Do not call this function during <a href="/windows/desktop/Dlls/dllmain">DllMain</a> or global objects constructors. This may cause invalid return values.
