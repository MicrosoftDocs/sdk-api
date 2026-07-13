---
UID: NF:winuser.IsHungAppWindow
title: IsHungAppWindow function (winuser.h)
description: Determines whether the system considers that a specified application is not responding.
helpviewer_keywords: ["IsHungAppWindow","IsHungAppWindow function [Windows and Messages]","_win32_IsHungAppWindow","_win32_ishungappwindow_cpp","winmsg.ishungappwindow","winui._win32_ishungappwindow","winuser/IsHungAppWindow"]
old-location: winmsg\ishungappwindow.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\ishungappwindow.htm
ms.date: 12/05/2018
ms.keywords: IsHungAppWindow, IsHungAppWindow function [Windows and Messages], _win32_IsHungAppWindow, _win32_ishungappwindow_cpp, winmsg.ishungappwindow, winui._win32_ishungappwindow, winuser/IsHungAppWindow
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
 - IsHungAppWindow
 - winuser/IsHungAppWindow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-window-l1-1-6.dll
 - ext-ms-win-ntuser-window-l1-1-5.dll
 - User32.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - IsHungAppWindow
req.apiset: ext-ms-win-ntuser-window-l1-1-3 (introduced in Windows 10, version 10.0.10240)
---

# IsHungAppWindow function


## -description

<p class="CCE_Message">[This function is not intended for general
      use. It may
      be altered or unavailable in subsequent versions of Windows.]

Determines whether the system considers that a specified application is not responding.
		An application is considered to be not responding if it is not waiting for input, is not in
		startup processing, and has not called <a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a> within
		the internal timeout period of 5 seconds.

## -parameters

### -param hwnd [in]

Type: <b>HWND</b>

A handle to the window to be tested.

## -returns

Type: <b>BOOL</b>

The return value is <b>TRUE</b> if the window stops responding; otherwise, it is <b>FALSE</b>.  Ghost windows always return
        <b>TRUE</b>.

## -remarks

The Windows timeout criteria of 5 seconds is subject to change.

This function was not included in the SDK headers and libraries until Windows XP Service Pack 1 (SP1) and Windows Server 2003. If you do not have a header file and import library for this function, you can call the function using <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-iswindow">IsWindow</a>



<b>Reference</b>



<a href="/windows/desktop/winmsg/windows">Windows</a>
