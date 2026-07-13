---
UID: NF:winuser.ShowOwnedPopups
title: ShowOwnedPopups function (winuser.h)
description: Shows or hides all pop-up windows owned by the specified window.
helpviewer_keywords: ["ShowOwnedPopups","ShowOwnedPopups function [Windows and Messages]","_win32_ShowOwnedPopups","_win32_showownedpopups_cpp","winmsg.showownedpopups","winui._win32_showownedpopups","winuser/ShowOwnedPopups"]
old-location: winmsg\showownedpopups.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\showownedpopups.htm
ms.date: 12/05/2018
ms.keywords: ShowOwnedPopups, ShowOwnedPopups function [Windows and Messages], _win32_ShowOwnedPopups, _win32_showownedpopups_cpp, winmsg.showownedpopups, winui._win32_showownedpopups, winuser/ShowOwnedPopups
req.header: winuser.h
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ShowOwnedPopups
 - winuser/ShowOwnedPopups
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-window-l1-1-6.dll
 - ext-ms-win-ntuser-window-l1-1-5.dll
 - User32.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - ShowOwnedPopups
req.apiset: ext-ms-win-ntuser-window-l1-1-3 (introduced in Windows 10, version 10.0.10240)
---

# ShowOwnedPopups function


## -description

Shows or hides all pop-up windows owned by the specified window.

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window that owns the pop-up windows to be shown or hidden.

### -param fShow [in]

Type: <b>BOOL</b>

If this parameter is <b>TRUE</b>, all hidden pop-up windows are shown. If this parameter is <b>FALSE</b>, all visible pop-up windows are hidden.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>ShowOwnedPopups</b> shows only windows hidden by a previous call to <b>ShowOwnedPopups</b>. For example, if a pop-up window is hidden by using the <a href="/windows/desktop/api/winuser/nf-winuser-showwindow">ShowWindow</a> function, subsequently calling <b>ShowOwnedPopups</b> with the <i>fShow</i> parameter set to <b>TRUE</b> does not cause the window to be shown.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-iswindowvisible">IsWindowVisible</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-showwindow">ShowWindow</a>



<a href="/windows/desktop/winmsg/windows">Windows</a>
