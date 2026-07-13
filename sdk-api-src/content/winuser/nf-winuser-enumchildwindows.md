---
UID: NF:winuser.EnumChildWindows
title: EnumChildWindows function (winuser.h)
description: Enumerates the child windows that belong to the specified parent window by passing the handle to each child window, in turn, to an application-defined callback function.
helpviewer_keywords: ["EnumChildWindows","EnumChildWindows function [Windows and Messages]","_win32_EnumChildWindows","_win32_enumchildwindows_cpp","winmsg.enumchildwindows","winui._win32_enumchildwindows","winuser/EnumChildWindows"]
old-location: winmsg\enumchildwindows.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\enumchildwindows.htm
ms.date: 12/05/2018
ms.keywords: EnumChildWindows, EnumChildWindows function [Windows and Messages], _win32_EnumChildWindows, _win32_enumchildwindows_cpp, winmsg.enumchildwindows, winui._win32_enumchildwindows, winuser/EnumChildWindows
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
 - EnumChildWindows
 - winuser/EnumChildWindows
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
 - EnumChildWindows
req.apiset: ext-ms-win-ntuser-window-l1-1-0 (introduced in Windows 8)
---

# EnumChildWindows function


## -description

Enumerates the child windows that belong to the specified parent window by passing the handle to each child window, in turn, to an application-defined callback function. <b>EnumChildWindows</b> continues until the last child window is enumerated or the callback function returns <b>FALSE</b>.

## -parameters

### -param hWndParent [in, optional]

Type: <b>HWND</b>

A handle to the parent window whose child windows are to be enumerated. If this parameter is <b>NULL</b>, this function is equivalent to <a href="/windows/desktop/api/winuser/nf-winuser-enumwindows">EnumWindows</a>.

### -param lpEnumFunc [in]

Type: <b>WNDENUMPROC</b>

A pointer to an application-defined callback function. For more information, see <a href="/previous-versions/windows/desktop/legacy/ms633493(v=vs.85)">EnumChildProc</a>.

### -param lParam [in]

Type: <b>LPARAM</b>

An application-defined value to be passed to the callback function.

## -returns

Type: <b>BOOL</b>

The return value is not used.

## -remarks

If a child window has created child windows of its own, <b>EnumChildWindows</b> enumerates those windows as well. 

A child window that is moved or repositioned in the Z order during the enumeration process will be properly enumerated. The function does not enumerate a child window that is destroyed before being enumerated or that is created during the enumeration process.

## -see-also

<b>Conceptual</b>



<a href="/previous-versions/windows/desktop/legacy/ms633493(v=vs.85)">EnumChildProc</a>



<a href="/windows/desktop/api/winuser/nf-winuser-enumthreadwindows">EnumThreadWindows</a>



<a href="/windows/desktop/api/winuser/nf-winuser-enumwindows">EnumWindows</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getwindow">GetWindow</a>



<b>Reference</b>



<a href="/windows/desktop/winmsg/windows">Windows</a>
