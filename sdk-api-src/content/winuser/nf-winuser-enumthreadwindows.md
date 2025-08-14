---
UID: NF:winuser.EnumThreadWindows
title: EnumThreadWindows function (winuser.h)
description: Enumerates all nonchild windows associated with a thread by passing the handle to each window, in turn, to an application-defined callback function.
helpviewer_keywords: ["EnumThreadWindows","EnumThreadWindows function [Windows and Messages]","_win32_EnumThreadWindows","_win32_enumthreadwindows_cpp","winmsg.enumthreadwindows","winui._win32_enumthreadwindows","winuser/EnumThreadWindows"]
old-location: winmsg\enumthreadwindows.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\enumthreadwindows.htm
ms.date: 12/05/2018
ms.keywords: EnumThreadWindows, EnumThreadWindows function [Windows and Messages], _win32_EnumThreadWindows, _win32_enumthreadwindows_cpp, winmsg.enumthreadwindows, winui._win32_enumthreadwindows, winuser/EnumThreadWindows
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
 - EnumThreadWindows
 - winuser/EnumThreadWindows
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
 - Ext-MS-Win-NTUser-Window-l1-1-0.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - minuser.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - EnumThreadWindows
req.apiset: ext-ms-win-ntuser-window-l1-1-0 (introduced in Windows 8)
---

# EnumThreadWindows function


## -description

Enumerates all nonchild windows associated with a thread by passing the handle to each window, in turn, to an application-defined callback function. <b>EnumThreadWindows</b> continues until the last window is enumerated or the callback function returns <b>FALSE</b>. To enumerate child windows of a particular window, use the <a href="/windows/desktop/api/winuser/nf-winuser-enumchildwindows">EnumChildWindows</a> function.

## -parameters

### -param dwThreadId [in]

Type: <b>DWORD</b>

The identifier of the thread whose windows are to be enumerated.

### -param lpfn [in]

Type: <b>WNDENUMPROC</b>

A pointer to an application-defined callback function. For more information, see <a href="/previous-versions/windows/desktop/legacy/ms633496(v=vs.85)">EnumThreadWndProc</a>.

### -param lParam [in]

Type: <b>LPARAM</b>

An application-defined value to be passed to the callback function.

## -returns

Type: <b>BOOL</b>

If the callback function returns <b>TRUE</b> for all windows in the thread specified by <i>dwThreadId</i>, the return value is <b>TRUE</b>. If the callback function returns <b>FALSE</b> on any enumerated window, or if there are no windows found in the thread specified by <i>dwThreadId</i>, the return value is <b>FALSE</b>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-enumchildwindows">EnumChildWindows</a>



<a href="/previous-versions/windows/desktop/legacy/ms633496(v=vs.85)">EnumThreadWndProc</a>



<a href="/windows/desktop/api/winuser/nf-winuser-enumwindows">EnumWindows</a>



<b>Reference</b>



<a href="/windows/desktop/winmsg/windows">Windows</a>
