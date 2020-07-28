---
UID: NF:winuser.GetCapture
title: GetCapture function (winuser.h)
description: Retrieves a handle to the window (if any) that has captured the mouse. Only one window at a time can capture the mouse; this window receives mouse input whether or not the cursor is within its borders.
helpviewer_keywords: ["GetCapture","GetCapture function [Keyboard and Mouse Input]","_win32_GetCapture","_win32_getcapture_cpp","inputdev.getcapture","winui._win32_getcapture","winuser/GetCapture"]
old-location: inputdev\getcapture.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\mouseinput\mouseinputreference\mouseinputfunctions\getcapture.htm
ms.date: 12/05/2018
ms.keywords: GetCapture, GetCapture function [Keyboard and Mouse Input], _win32_GetCapture, _win32_getcapture_cpp, inputdev.getcapture, winui._win32_getcapture, winuser/GetCapture
f1_keywords:
- winuser/GetCapture
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
req.unicode-ansi: 
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
- Ext-MS-Win-NTUser-mouse-l1-1-0.dll
- api-ms-win-ntuser-ie-mouse-l1-1-0.dll
- ie_stubs.dll
api_name:
- GetCapture
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetCapture function


## -description


Retrieves a handle to the window (if any) that has captured the mouse. Only one window at a time can capture the mouse; this window receives mouse input whether or not the cursor is within its borders. 


## -parameters






## -returns



Type: <b>HWND</b>

The return value is a handle to the capture window associated with the current thread. If no window in the thread has captured the mouse, the return value is <b>NULL</b>. 




## -remarks



A <b>NULL</b> return value means the current thread has not captured the mouse. However, it is possible that another thread or process has captured the mouse. 

To get a handle to the capture window on another thread, use the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getguithreadinfo">GetGUIThreadInfo</a> function.




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getguithreadinfo">GetGUIThreadInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/inputdev/mouse-input">Mouse Input</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-releasecapture">ReleaseCapture</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setcapture">SetCapture</a>
 

 

