---
UID: NF:winuser.EnumWindows
title: EnumWindows function (winuser.h)
description: Enumerates all top-level windows on the screen by passing the handle to each window, in turn, to an application-defined callback function. EnumWindows continues until the last top-level window is enumerated or the callback function returns FALSE.
helpviewer_keywords: ["EnumWindows","EnumWindows function [Windows and Messages]","_win32_EnumWindows","_win32_enumwindows_cpp","winmsg.enumwindows","winui._win32_enumwindows","winuser/EnumWindows"]
old-location: winmsg\enumwindows.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\enumwindows.htm
ms.date: 12/05/2018
ms.keywords: EnumWindows, EnumWindows function [Windows and Messages], _win32_EnumWindows, _win32_enumwindows_cpp, winmsg.enumwindows, winui._win32_enumwindows, winuser/EnumWindows
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
 - EnumWindows
 - winuser/EnumWindows
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
 - EnumWindows
req.apiset: ext-ms-win-ntuser-window-l1-1-0 (introduced in Windows 8)
---

# EnumWindows function


## -description

Enumerates all top-level windows on the screen by passing the handle to each window, in turn, to an application-defined callback function. <b>EnumWindows</b> continues until the last top-level window is enumerated or the callback function returns <b>FALSE</b>.

## -parameters

### -param lpEnumFunc [in]

Type: <b>WNDENUMPROC</b>

A pointer to an application-defined callback function. For more information, see <a href="/previous-versions/windows/desktop/legacy/ms633498(v=vs.85)">EnumWindowsProc</a>.

### -param lParam [in]

Type: <b>LPARAM</b>

An application-defined value to be passed to the callback function.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

If <a href="/previous-versions/windows/desktop/legacy/ms633498(v=vs.85)">EnumWindowsProc</a> returns zero, the return value is also zero. In this case, the callback function should call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a> to obtain a meaningful error code to be returned to the caller of <b>EnumWindows</b>.

## -remarks

The <b>EnumWindows</b> function does not enumerate child windows, with the exception of a few top-level windows owned by the system that have the <b>WS_CHILD</b> style.

This function is more reliable than calling the <a href="/windows/desktop/api/winuser/nf-winuser-getwindow">GetWindow</a> function in a loop. An application that calls <b>GetWindow</b> to perform this task risks being caught in an infinite loop or referencing a handle to a window that has been destroyed. 

<div class="alert"><b>Note</b>  For Windows 8 and later, <b>EnumWindows</b> enumerates only top-level windows of desktop apps.</div>
<div> </div>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-enumchildwindows">EnumChildWindows</a>



<a href="/previous-versions/windows/desktop/legacy/ms633498(v=vs.85)">EnumWindowsProc</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getwindow">GetWindow</a>



<b>Reference</b>



<a href="/windows/desktop/winmsg/windows">Windows</a>
