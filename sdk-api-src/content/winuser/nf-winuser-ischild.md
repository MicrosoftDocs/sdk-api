---
UID: NF:winuser.IsChild
title: IsChild function (winuser.h)
description: Determines whether a window is a child window or descendant window of a specified parent window.
helpviewer_keywords: ["IsChild","IsChild function [Windows and Messages]","_win32_IsChild","_win32_ischild_cpp","winmsg.ischild","winui._win32_ischild","winuser/IsChild"]
old-location: winmsg\ischild.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\ischild.htm
ms.date: 12/05/2018
ms.keywords: IsChild, IsChild function [Windows and Messages], _win32_IsChild, _win32_ischild_cpp, winmsg.ischild, winui._win32_ischild, winuser/IsChild
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
 - IsChild
 - winuser/IsChild
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-window-ext-l1-1-1.dll
 - ext-ms-win-ntuser-window-l1-1-6.dll
 - ext-ms-win-ntuser-window-l1-1-5.dll
 - User32.dll
 - API-MS-Win-NTUser-IE-Window-l1-1-0.dll
 - ie_shims.dll
 - API-MS-Win-RTCore-NTUser-Window-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-NTUser-Window-l1-1-0.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - IsChild
req.apiset: ext-ms-win-ntuser-window-l1-1-0 (introduced in Windows 8)
---

# IsChild function


## -description

Determines whether a window is a child window or descendant window of a specified parent window. A child window is the direct descendant of a specified parent window if that parent window is in the chain of parent windows; the chain of parent windows leads from the original overlapped or pop-up window to the child window.

## -parameters

### -param hWndParent [in]

Type: <b>HWND</b>

A handle to the parent window.

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window to be tested.

## -returns

Type: <b>BOOL</b>

If the window is a child or descendant window of the specified parent window, the return value is nonzero.

If the window is not a child or descendant window of the specified parent window, the return value is zero.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-iswindow">IsWindow</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setparent">SetParent</a>



<a href="/windows/desktop/winmsg/windows">Windows</a>
