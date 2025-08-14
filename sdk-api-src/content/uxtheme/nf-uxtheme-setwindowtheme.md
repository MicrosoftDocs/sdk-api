---
UID: NF:uxtheme.SetWindowTheme
title: SetWindowTheme function (uxtheme.h)
description: Causes a window to use a different set of visual style information than its class normally uses.
helpviewer_keywords: ["SetWindowTheme","SetWindowTheme function [Windows Controls]","controls.SetWindowTheme","controls.inet_SetWindowTheme","inet_SetWindowTheme","inet_SetWindowTheme_cpp","uxtheme/SetWindowTheme"]
old-location: controls\SetWindowTheme.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\setwindowtheme.htm
ms.date: 12/05/2018
ms.keywords: SetWindowTheme, SetWindowTheme function [Windows Controls], controls.SetWindowTheme, controls.inet_SetWindowTheme, inet_SetWindowTheme, inet_SetWindowTheme_cpp, uxtheme/SetWindowTheme
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
 - SetWindowTheme
 - uxtheme/SetWindowTheme
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
 - SetWindowTheme
---

# SetWindowTheme function


## -description

Causes a window to use a different set of visual style information than its class normally uses.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the window whose visual style information is to be changed.

### -param pszSubAppName [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCWSTR</a></b>

Pointer to a string that contains the application name to use in place of the calling application's name. If this parameter is <b>NULL</b>, the calling application's name is used.

### -param pszSubIdList [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCWSTR</a></b>

Pointer to a string that contains a semicolon-separated list of CLSID names to use in place of the actual list passed by the window's class. If this parameter is <b>NULL</b>, the ID list from the calling class is used.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The theme manager retains the <i>pszSubAppName</i> and the <i>pszSubIdList</i> associations through the lifetime of the window, even if visual styles subsequently change. The window is sent a <a href="/windows/desktop/winmsg/wm-themechanged">WM_THEMECHANGED</a> message at the end of a <b>SetWindowTheme</b> call, so that the new visual style can be found and applied.


When <i>pszSubAppName</i> and <i>pszSubIdList</i> are <b>NULL</b>, the theme manager removes the previously applied associations. You can prevent visual styles from being applied to a specified window by specifying an empty string, (L""), which does not match any section entries. 


#### Examples

The following example code gives a list-view control the appearance of a Windows Explorer list: 


```cpp
SetWindowTheme(hwndList, L"Explorer", NULL);

```
