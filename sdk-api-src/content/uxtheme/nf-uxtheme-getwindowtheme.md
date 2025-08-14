---
UID: NF:uxtheme.GetWindowTheme
title: GetWindowTheme function (uxtheme.h)
description: Retrieves a theme handle to a window that has visual styles applied.
helpviewer_keywords: ["GetWindowTheme","GetWindowTheme function [Windows Controls]","controls.GetWindowTheme","controls.inet_GetWindowTheme","inet_GetWindowTheme","inet_GetWindowTheme_cpp","uxtheme/GetWindowTheme"]
old-location: controls\GetWindowTheme.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\getwindowtheme.htm
ms.date: 12/05/2018
ms.keywords: GetWindowTheme, GetWindowTheme function [Windows Controls], controls.GetWindowTheme, controls.inet_GetWindowTheme, inet_GetWindowTheme, inet_GetWindowTheme_cpp, uxtheme/GetWindowTheme
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
req.dll: UxTheme.dll (version 1.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetWindowTheme
 - uxtheme/GetWindowTheme
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
 - GetWindowTheme
---

# GetWindowTheme function


## -description

Retrieves a theme handle to a window that has visual styles applied.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle of the window.

## -returns

Type: <b>HTHEME</b>

The most recent theme handle from <a href="/windows/desktop/api/uxtheme/nf-uxtheme-openthemedata">OpenThemeData</a>.

## -remarks

If a window has a visual style applied, the <b>GetWindowTheme</b> function returns the most recent theme handle from <a href="/windows/desktop/api/uxtheme/nf-uxtheme-openthemedata">OpenThemeData</a>. If no visual style is applied, <b>GetWindowTheme</b> returns <b>NULL</b>.