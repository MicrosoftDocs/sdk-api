---
UID: NF:winuser.GetWindowTextLengthW
title: GetWindowTextLengthW function
author: windows-sdk-content
description: Retrieves the length, in characters, of the specified window's title bar text (if the window has a title bar).
old-location: winmsg\getwindowtextlength.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\getwindowtextlength.htm
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: GetWindowTextLength, GetWindowTextLength function [Windows and Messages], GetWindowTextLengthA, GetWindowTextLengthW, _win32_GetWindowTextLength, _win32_getwindowtextlength_cpp, winmsg.getwindowtextlength, winui._win32_getwindowtextlength, winuser/GetWindowTextLength, winuser/GetWindowTextLengthA, winuser/GetWindowTextLengthW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: 
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetWindowTextLengthW function


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

If the window has no text, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



If the target window is owned by the current process, <b>GetWindowTextLength</b> causes a <a href="https://msdn.microsoft.com/9e185435-a624-4380-adfd-be4f3645ee5d">WM_GETTEXTLENGTH</a> message to be sent to the specified window or control. 

Under certain conditions, the <b>GetWindowTextLength</b> function may return a value that is larger than the actual length of the text. This occurs with certain mixtures of ANSI and Unicode, and is due to the system allowing for the possible existence of double-byte character set (DBCS) characters within the text. The return value, however, will always be at least as large as the actual length of the text; you can thus always use it to guide buffer allocation. This behavior can occur when an application uses both ANSI functions and common dialogs, which use Unicode. It can also occur when an application uses the ANSI version of <b>GetWindowTextLength</b> with a window whose window procedure is Unicode, or the Unicode version of <b>GetWindowTextLength</b> with a window whose window procedure is ANSI. For more information on ANSI and ANSI functions, see <a href="https://msdn.microsoft.com/601d24b0-11bb-48fa-a257-207c3acee226">Conventions for Function Prototypes</a>. 

To obtain the exact length of the text, use the <a href="https://msdn.microsoft.com/117c3d6d-24cd-462f-bdb0-b65d8914273a">WM_GETTEXT</a>, <a href="controls._win32_LB_GETTEXT">LB_GETTEXT</a>, or <a href="controls._win32_CB_GETLBTEXT">CB_GETLBTEXT</a> messages, or the <a href="https://msdn.microsoft.com/461d2200-2e3a-4361-bb2e-9a29ed9f333f">GetWindowText</a> function.




## -see-also




<a href="controls._win32_CB_GETLBTEXT">CB_GETLBTEXT</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/461d2200-2e3a-4361-bb2e-9a29ed9f333f">GetWindowText</a>



<a href="controls._win32_LB_GETTEXT">LB_GETTEXT</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/6f3e3ef8-b342-43f0-9d8b-3a72c610a940">SetWindowText</a>



<a href="https://msdn.microsoft.com/117c3d6d-24cd-462f-bdb0-b65d8914273a">WM_GETTEXT</a>



<a href="https://msdn.microsoft.com/9e185435-a624-4380-adfd-be4f3645ee5d">WM_GETTEXTLENGTH</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt637455">Windows</a>
 

 

