---
UID: NF:winuser.GetShellWindow
title: GetShellWindow function (winuser.h)
description: Retrieves a handle to the Shell's desktop window.
helpviewer_keywords: ["GetShellWindow","GetShellWindow function [Windows and Messages]","_win32_GetShellWindow","_win32_getshellwindow_cpp","winmsg.getshellwindow","winui._win32_getshellwindow","winuser/GetShellWindow"]
old-location: winmsg\getshellwindow.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\getshellwindow.htm
ms.date: 12/05/2018
ms.keywords: GetShellWindow, GetShellWindow function [Windows and Messages], _win32_GetShellWindow, _win32_getshellwindow_cpp, winmsg.getshellwindow, winui._win32_getshellwindow, winuser/GetShellWindow
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
 - GetShellWindow
 - winuser/GetShellWindow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-iam-l1-1-2.dll
 - ext-ms-win-ntuser-window-l1-1-6.dll
 - ext-ms-win-ntuser-window-l1-1-5.dll
 - User32.dll
 - API-MS-Win-RTCore-NTUser-shell-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-NTUser-Window-l1-1-0.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - Ext-MS-Win-RTCore-NTUser-iam-l1-1-0.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
 - Ext-MS-Win-RTCore-NTUser-Iam-L1-1-1.dll
api_name:
 - GetShellWindow
req.apiset: ext-ms-win-ntuser-window-l1-1-0 (introduced in Windows 8)
---

# GetShellWindow function


## -description

Retrieves a handle to the Shell's desktop window.



## -returns

Type: <b>HWND</b>

The return value is the handle of the Shell's desktop window. If no Shell process is present, the return value is <b>NULL</b>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getdesktopwindow">GetDesktopWindow</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getwindow">GetWindow</a>



<b>Reference</b>



<a href="/windows/desktop/winmsg/windows">Windows</a>
