---
UID: NF:winuser.InternalGetWindowText
title: InternalGetWindowText function
author: windows-sdk-content
description: Copies the text of the specified window's title bar (if it has one) into a buffer.
old-location: winmsg\internalgetwindowtext.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\internalgetwindowtext.htm
ms.author: windowssdkdev
ms.date: 03/29/2018
ms.keywords: InternalGetWindowText, InternalGetWindowText function [Windows and Messages], _win32_InternalGetWindowText, _win32_internalgetwindowtext_cpp, winmsg.internalgetwindowtext, winui._win32_internalgetwindowtext, winuser/InternalGetWindowText
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
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: POINTER_DEVICE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - InternalGetWindowText
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# InternalGetWindowText function


## -description


<p class="CCE_Message">[This function is not intended for general
      use. It may
      be altered or unavailable in subsequent versions of Windows.]

Copies the text of the specified window's title bar (if it has one) into a buffer.

This function is similar to the <a href="https://msdn.microsoft.com/461d2200-2e3a-4361-bb2e-9a29ed9f333f">GetWindowText</a> function.
		However, it obtains the window text directly from the window structure
		associated with the specified window's handle and then always provides the text as a
		Unicode string. This is unlike <b>GetWindowText</b> which obtains the
		text by sending the window a <a href="https://msdn.microsoft.com/117c3d6d-24cd-462f-bdb0-b65d8914273a">WM_GETTEXT</a> message.  If the
		specified window is a control, the text of the control is obtained. 


## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window or control containing the text. 


### -param pString

TBD


### -param cchMaxCount

TBD




#### - lpString [out]

Type: <b>LPWSTR</b>

The buffer that is to receive the text.
				
				If the
				string is as long or longer than the buffer, the string is truncated and
				terminated with a null character. 


#### - nMaxCount [in]

Type: <b>int</b>

The maximum number of characters to be copied to the buffer,
				including the null character. If the text exceeds this limit,
				it is truncated. 


## -returns



Type: <strong>Type: <b>int</b>
</strong>

If the function succeeds, the return value is the length, in characters,
				of the copied string, not including the terminating null character.
				If the window has no title bar or text, if the title bar is empty, or if the window
				or control handle is invalid, the return value is zero. To get extended error
				information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



This function was not included in the SDK headers and libraries until Windows XP with Service Pack 1 (SP1) and Windows Server 2003. If you do not have a header file and import library for this function, you can call the function using <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a>.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/461d2200-2e3a-4361-bb2e-9a29ed9f333f">GetWindowText</a>



<a href="https://msdn.microsoft.com/dfd05c5b-2e60-4f4f-aa6b-53f723a048be">GetWindowTextLength</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/6f3e3ef8-b342-43f0-9d8b-3a72c610a940">SetWindowText</a>



<a href="https://msdn.microsoft.com/62b4616c-37bf-4d9f-8891-7010c7035d18">Using Messages and Message Queues</a>



<a href="https://msdn.microsoft.com/117c3d6d-24cd-462f-bdb0-b65d8914273a">WM_GETTEXT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt637455">Windows</a>
 

 

