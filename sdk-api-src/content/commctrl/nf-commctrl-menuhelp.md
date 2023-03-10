---
UID: NF:commctrl.MenuHelp
title: MenuHelp function (commctrl.h)
description: Processes WM_MENUSELECT and WM_COMMAND messages and displays Help text about the current menu in the specified status window.
helpviewer_keywords: ["MenuHelp","MenuHelp function [Windows Controls]","_win32_MenuHelp","_win32_MenuHelp_cpp","commctrl/MenuHelp","controls.MenuHelp","controls._win32_MenuHelp"]
old-location: controls\MenuHelp.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\status\functions\menuhelp.htm
ms.date: 12/05/2018
ms.keywords: MenuHelp, MenuHelp function [Windows Controls], _win32_MenuHelp, _win32_MenuHelp_cpp, commctrl/MenuHelp, controls.MenuHelp, controls._win32_MenuHelp
req.header: commctrl.h
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
req.lib: Comctl32.lib
req.dll: Comctl32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MenuHelp
 - commctrl/MenuHelp
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - MenuHelp
---

# MenuHelp function


## -description

Processes <a href="/windows/desktop/menurc/wm-menuselect">WM_MENUSELECT</a> and <a href="/windows/desktop/menurc/wm-command">WM_COMMAND</a> messages and displays Help text about the current menu in the specified status window.

## -parameters

### -param uMsg

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Message being processed. This can be either <a href="/windows/desktop/menurc/wm-menuselect">WM_MENUSELECT</a> or <a href="/windows/desktop/menurc/wm-command">WM_COMMAND</a>.

### -param wParam

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">WPARAM</a></b>

wParam of the message specified in 
					<i>uMsg</i>.

### -param lParam

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

lParam of the message specified in 
					<i>uMsg</i>.

### -param hMainMenu

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HMENU</a></b>

Handle to the application's main menu.

### -param hInst

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HINSTANCE</a></b>

Handle to the module that contains the string resources.

### -param hwndStatus

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the status window.

### -param lpwIDs

Type: <b>LPUINT</b>

Pointer to an array of values that contains pairs of string resource identifiers and menu handles. The function searches the array for the handle to the selected menu and, if found, uses the corresponding resource identifier to load the appropriate Help string.

## -remarks

The <b>MenuHelp</b> function is a helper function. Helper functions are available as a convenience to programming. They combine into one call a sequence of frequently used calls. You use <b>MenuHelp</b> to send <a href="/windows/desktop/menurc/wm-menuselect">WM_MENUSELECT</a> and <a href="/windows/desktop/menurc/wm-command">WM_COMMAND</a> messages.