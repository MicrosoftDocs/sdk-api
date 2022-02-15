---
UID: NF:uxtheme.SetWindowThemeNonClientAttributes
title: SetWindowThemeNonClientAttributes function (uxtheme.h)
description: Sets non-client attributes to control how visual styles are applied to a specified window.
helpviewer_keywords: ["SetWindowThemeNonClientAttributes","SetWindowThemeNonClientAttributes function [Windows Controls]","_shell_SetWindowThemeNonClientAttributes","_shell_SetWindowThemeNonClientAttributes_cpp","controls.SetWindowThemeNonClientAttributes","controls._shell_SetWindowThemeNonClientAttributes","uxtheme/SetWindowThemeNonClientAttributes"]
old-location: controls\SetWindowThemeNonClientAttributes.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\setwindowthemenonclientattributes.htm
ms.date: 12/05/2018
ms.keywords: SetWindowThemeNonClientAttributes, SetWindowThemeNonClientAttributes function [Windows Controls], _shell_SetWindowThemeNonClientAttributes, _shell_SetWindowThemeNonClientAttributes_cpp, controls.SetWindowThemeNonClientAttributes, controls._shell_SetWindowThemeNonClientAttributes, uxtheme/SetWindowThemeNonClientAttributes
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
 - SetWindowThemeNonClientAttributes
 - uxtheme/SetWindowThemeNonClientAttributes
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
 - SetWindowThemeNonClientAttributes
---

# SetWindowThemeNonClientAttributes function


## -description

Sets non-client attributes to control how visual styles are applied to a specified window.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the window in which to apply changes.

### -param dwMask [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

A bitmask that describes which values are to be modified. Can be a combination of the <a href="/windows/desktop/Controls/wtnca">WTNCA</a> constants.

### -param dwAttributes [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

A combination of flags that modify window visual style attributes based on <i>dwMask</i>. Can be a combination of the <a href="/windows/desktop/Controls/wtnca">WTNCA</a> constants.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.