---
UID: NF:winuser.FindWindowExA
title: FindWindowExA function (winuser.h)
description: Retrieves a handle to a window whose class name and window name match the specified strings. The function searches child windows, beginning with the one following the specified child window. This function does not perform a case-sensitive search.helpviewer_keywords: ["FindWindowEx","FindWindowEx function [Windows and Messages]","FindWindowExA","FindWindowExW","_win32_FindWindowEx","_win32_findwindowex_cpp","winmsg.findwindowex","winui._win32_findwindowex","winuser/FindWindowEx","winuser/FindWindowExA","winuser/FindWindowExW"]
old-location: winmsg\findwindowex.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\findwindowex.htm
ms.date: 12/05/2018
ms.keywords: FindWindowEx, FindWindowEx function [Windows and Messages], FindWindowExA, FindWindowExW, _win32_FindWindowEx, _win32_findwindowex_cpp, winmsg.findwindowex, winui._win32_findwindowex, winuser/FindWindowEx, winuser/FindWindowExA, winuser/FindWindowExW
f1_keywords:
- winuser/FindWindowEx
dev_langs:
- c++
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FindWindowExW (Unicode) and FindWindowExA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- User32.dll
- API-MS-Win-NTUser-IE-Window-l1-1-0.dll
- ie_shims.dll
- API-MS-Win-RTCore-NTUser-Window-l1-1-0.dll
- minuser.dll
- Ext-MS-Win-NTUser-Window-l1-1-1.dll
- Ext-MS-Win-NTUser-Window-l1-1-2.dll
- Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
- ext-ms-win-ntuser-window-l1-1-3.dll
- Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
- FindWindowEx
- FindWindowExA
- FindWindowExW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FindWindowExA function


## -description


Retrieves a handle to a window whose class name and window name match the specified strings. The function searches child windows, beginning with the one following the specified child window. This function does not perform a case-sensitive search. 


## -parameters




### -param hWndParent [in, optional]

Type: <b>HWND</b>

A handle to the parent window whose child windows are to be searched.

If <i>hwndParent</i> is <b>NULL</b>, the function uses the desktop window as the parent window. The function searches among windows that are child windows of the desktop. 

If <i>hwndParent</i> is <b>HWND_MESSAGE</b>, the function searches all <a href="https://docs.microsoft.com/windows/desktop/winmsg/window-features">message-only windows</a>. 


### -param hWndChildAfter [in, optional]

Type: <b>HWND</b>

A handle to a child window. The search begins with the next child window in the Z order. The child window must be a direct child window of <i>hwndParent</i>, not just a descendant window. 

If <i>hwndChildAfter</i> is <b>NULL</b>, the search begins with the first child window of <i>hwndParent</i>. 

Note that if both <i>hwndParent</i> and <i>hwndChildAfter</i> are <b>NULL</b>, the function searches all top-level and message-only windows. 


### -param lpszClass [in, optional]

Type: <b>LPCTSTR</b>

The class name or a class atom created by a previous call to the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-registerclassa">RegisterClass</a> or <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-registerclassexa">RegisterClassEx</a> function. The atom must be placed in the low-order word of <i>lpszClass</i>; the high-order word must be zero.

 If <i>lpszClass</i> is a string, it specifies the window class name. The class name can be any name registered with <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-registerclassa">RegisterClass</a> or <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-registerclassexa">RegisterClassEx</a>, or any of the predefined control-class names, or it can be <code>MAKEINTATOM(0x8000)</code>. In this latter case, 0x8000 is the atom for a menu class. For more information, see the Remarks section of this topic.


### -param lpszWindow [in, optional]

Type: <b>LPCTSTR</b>

The window name (the window's title). If this parameter is <b>NULL</b>, all window names match. 


## -returns



Type: <b>HWND</b>

If the function succeeds, the return value is a handle to the window that has the specified class and window names.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. 




## -remarks



If the <i>lpszWindow</i> parameter is not <b>NULL</b>, <b>FindWindowEx</b> calls the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getwindowtexta">GetWindowText</a> function to retrieve the window name for comparison. For a description of a potential problem that can arise, see the Remarks section of <b>GetWindowText</b>.

An application can call this function in the following way.

<code>FindWindowEx( NULL, NULL, MAKEINTATOM(0x8000), NULL );</code>

Note that 0x8000 is the atom for a menu class. When an application calls this function, the function checks whether a context menu is being displayed that the application created.




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-enumwindows">EnumWindows</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-findwindowa">FindWindow</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getclassname">GetClassName</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getwindowtexta">GetWindowText</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-registerclassa">RegisterClass</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-registerclassexa">RegisterClassEx</a>



<a href="https://docs.microsoft.com/windows/desktop/winmsg/windows">Windows</a>
 

 

