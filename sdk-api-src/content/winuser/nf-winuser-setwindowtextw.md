---
UID: NF:winuser.SetWindowTextW
title: SetWindowTextW function
author: windows-sdk-content
description: Changes the text of the specified window's title bar (if it has one). If the specified window is a control, the text of the control is changed. However, SetWindowText cannot change the text of a control in another application.
old-location: winmsg\setwindowtext.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\setwindowtext.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SetWindowText, SetWindowText function [Windows and Messages], SetWindowTextA, SetWindowTextW, _win32_SetWindowText, _win32_setwindowtext_cpp, winmsg.setwindowtext, winui._win32_setwindowtext, winuser/SetWindowText, winuser/SetWindowTextA, winuser/SetWindowTextW
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetWindowTextW (Unicode) and SetWindowTextA (ANSI)
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
 - Ext-MS-Win-NTUser-Window-l1-1-0.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - SetWindowText
 - SetWindowTextA
 - SetWindowTextW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetWindowTextW function


## -description


Changes the text of the specified window's title bar (if it has one). If the specified window is a control, the text of the control is changed. However, <b>SetWindowText</b> cannot change the text of a control in another application.


## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window or control whose text is to be changed. 


### -param lpString [in, optional]

Type: <b>LPCTSTR</b>

The new title or control text. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



If the target window is owned by the current process, <b>SetWindowText</b> causes a <a href="https://msdn.microsoft.com/en-us/library/ms632644(v=VS.85).aspx">WM_SETTEXT</a> message to be sent to the specified window or control. If the control is a list box control created with the <b>WS_CAPTION</b> style, however, <b>SetWindowText</b> sets the text for the control, not for the list box entries. 

To set the text of a control in another process, send the <a href="https://msdn.microsoft.com/en-us/library/ms632644(v=VS.85).aspx">WM_SETTEXT</a> message directly instead of calling <b>SetWindowText</b>. 

The <b>SetWindowText</b> function does not expand tab characters (ASCII code 0x09). Tab characters are displayed as vertical bar (|) characters. 


#### Examples

 For an example, see <a href="https://msdn.microsoft.com/en-us/library/ms644928(v=VS.85).aspx">Sending a Message</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms633520(v=VS.85).aspx">GetWindowText</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms632644(v=VS.85).aspx">WM_SETTEXT</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632595(v=VS.85).aspx">Windows</a>
 

 

