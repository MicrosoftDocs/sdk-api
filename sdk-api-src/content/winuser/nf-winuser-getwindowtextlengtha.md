---
UID: NF:winuser.GetWindowTextLengthA
title: GetWindowTextLengthA function (winuser.h)
author: windows-sdk-content
description: Retrieves the length, in characters, of the specified window's title bar text (if the window has a title bar).
old-location: winmsg\getwindowtextlength.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\getwindowtextlength.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetWindowTextLength, GetWindowTextLength function [Windows and Messages], GetWindowTextLengthA, GetWindowTextLengthW, _win32_GetWindowTextLength, _win32_getwindowtextlength_cpp, winmsg.getwindowtextlength, winui._win32_getwindowtextlength, winuser/GetWindowTextLength, winuser/GetWindowTextLengthA, winuser/GetWindowTextLengthW
ms.topic: function
f1_keywords: 
 - "winuser/GetWindowTextLength"
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetWindowTextLengthW (Unicode) and GetWindowTextLengthA (ANSI)
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
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-0.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - GetWindowTextLength
 - GetWindowTextLengthA
 - GetWindowTextLengthW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetWindowTextLengthA function


## -description


Retrieves the length, in characters, of the specified window's title bar text (if the window has a title bar). If the specified window is a control, the function retrieves the length of the text within the control. However, <b>GetWindowTextLength</b> cannot retrieve the length of the text of an edit control in another application.


## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window or control.


## -returns



Type: <strong>Type: <b>int</b>
</strong>

If the function succeeds, the return value is the length, in characters, of the text. Under certain conditions, this value may actually be greater than the length of the text. For more information, see the following Remarks section.

If the window has no text, the return value is zero. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. 




## -remarks



If the target window is owned by the current process, <b>GetWindowTextLength</b> causes a <a href="https://docs.microsoft.com/windows/desktop/winmsg/wm-gettextlength">WM_GETTEXTLENGTH</a> message to be sent to the specified window or control. 

Under certain conditions, the <b>GetWindowTextLength</b> function may return a value that is larger than the actual length of the text. This occurs with certain mixtures of ANSI and Unicode, and is due to the system allowing for the possible existence of double-byte character set (DBCS) characters within the text. The return value, however, will always be at least as large as the actual length of the text; you can thus always use it to guide buffer allocation. This behavior can occur when an application uses both ANSI functions and common dialogs, which use Unicode. It can also occur when an application uses the ANSI version of <b>GetWindowTextLength</b> with a window whose window procedure is Unicode, or the Unicode version of <b>GetWindowTextLength</b> with a window whose window procedure is ANSI. For more information on ANSI and ANSI functions, see <a href="https://docs.microsoft.com/windows/desktop/Intl/conventions-for-function-prototypes">Conventions for Function Prototypes</a>. 

To obtain the exact length of the text, use the <a href="https://docs.microsoft.com/windows/desktop/winmsg/wm-gettext">WM_GETTEXT</a>, <a href="https://docs.microsoft.com/windows/desktop/Controls/lb-gettext">LB_GETTEXT</a>, or <a href="https://docs.microsoft.com/windows/desktop/Controls/cb-getlbtext">CB_GETLBTEXT</a> messages, or the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getwindowtexta">GetWindowText</a> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Controls/cb-getlbtext">CB_GETLBTEXT</a>



<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getwindowtexta">GetWindowText</a>



<a href="https://docs.microsoft.com/windows/desktop/Controls/lb-gettext">LB_GETTEXT</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setwindowtexta">SetWindowText</a>



<a href="https://docs.microsoft.com/windows/desktop/winmsg/wm-gettext">WM_GETTEXT</a>



<a href="https://docs.microsoft.com/windows/desktop/winmsg/wm-gettextlength">WM_GETTEXTLENGTH</a>



<a href="https://docs.microsoft.com/windows/desktop/winmsg/windows">Windows</a>
 

 

