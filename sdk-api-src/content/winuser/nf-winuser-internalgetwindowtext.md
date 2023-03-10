---
UID: NF:winuser.InternalGetWindowText
title: InternalGetWindowText function (winuser.h)
description: Copies the text of the specified window's title bar (if it has one) into a buffer.
helpviewer_keywords: ["InternalGetWindowText","InternalGetWindowText function [Windows and Messages]","_win32_InternalGetWindowText","_win32_internalgetwindowtext_cpp","winmsg.internalgetwindowtext","winui._win32_internalgetwindowtext","winuser/InternalGetWindowText"]
old-location: winmsg\internalgetwindowtext.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\internalgetwindowtext.htm
ms.date: 12/05/2018
ms.keywords: InternalGetWindowText, InternalGetWindowText function [Windows and Messages], _win32_InternalGetWindowText, _win32_internalgetwindowtext_cpp, winmsg.internalgetwindowtext, winui._win32_internalgetwindowtext, winuser/InternalGetWindowText
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
 - InternalGetWindowText
 - winuser/InternalGetWindowText
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - InternalGetWindowText
---

# InternalGetWindowText function


## -description

<p class="CCE_Message">[This function is not intended for general
      use. It may
      be altered or unavailable in subsequent versions of Windows.]

Copies the text of the specified window's title bar (if it has one) into a buffer.

This function is similar to the <a href="/windows/desktop/api/winuser/nf-winuser-getwindowtexta">GetWindowText</a> function.
		However, it obtains the window text directly from the window structure
		associated with the specified window's handle and then always provides the text as a
		Unicode string. This is unlike <b>GetWindowText</b> which obtains the
		text by sending the window a <a href="/windows/desktop/winmsg/wm-gettext">WM_GETTEXT</a> message.  If the
		specified window is a control, the text of the control is obtained.

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window or control containing the text.

### -param pString [out]

Type: <b>LPWSTR</b>

The buffer that is to receive the text.
				
If the string is as long or longer than the buffer, the string is truncated and terminated with a null character.

### -param cchMaxCount [in]

Type: <b>int</b>

The maximum number of characters to be copied to the buffer, including the null character. If the text exceeds this limit, it is truncated.

## -returns

Type: <b>int</b>

If the function succeeds, the return value is the length, in characters, of the copied string, not including the terminating null character.

If the window has no title bar or text, if the title bar is empty, or if the window or control handle is invalid, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function was not included in the SDK headers and libraries until Windows XP with Service Pack 1 (SP1) and Windows Server 2003. If you do not have a header file and import library for this function, you can call the function using <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getwindowtexta">GetWindowText</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha">GetWindowTextLength</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setwindowtexta">SetWindowText</a>



<a href="/windows/desktop/winmsg/using-messages-and-message-queues">Using Messages and Message Queues</a>



<a href="/windows/desktop/winmsg/wm-gettext">WM_GETTEXT</a>



<a href="/windows/desktop/winmsg/windows">Windows</a>