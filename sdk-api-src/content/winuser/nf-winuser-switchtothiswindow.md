---
UID: NF:winuser.SwitchToThisWindow
title: SwitchToThisWindow function (winuser.h)
description: Switches focus to the specified window and brings it to the foreground.
helpviewer_keywords: ["SwitchToThisWindow","SwitchToThisWindow function [Windows and Messages]","_win32_SwitchToThisWindow","_win32_switchtothiswindow_cpp","winmsg.switchtothiswindow","winui._win32_switchtothiswindow","winuser/SwitchToThisWindow"]
old-location: winmsg\switchtothiswindow.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\switchtothiswindow.htm
ms.date: 12/05/2018
ms.keywords: SwitchToThisWindow, SwitchToThisWindow function [Windows and Messages], _win32_SwitchToThisWindow, _win32_switchtothiswindow_cpp, winmsg.switchtothiswindow, winui._win32_switchtothiswindow, winuser/SwitchToThisWindow
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
 - SwitchToThisWindow
 - winuser/SwitchToThisWindow
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
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - SwitchToThisWindow
req.apiset: ext-ms-win-ntuser-window-l1-1-4 (introduced in Windows 10, version 10.0.14393)
---

# SwitchToThisWindow function


## -description

<p class="CCE_Message">[This function is not intended for general
      use. It may
      be altered or unavailable in subsequent versions of Windows.]

Switches
		 focus to the specified window and brings it to the foreground.

## -parameters

### -param hwnd [in]

Type: <b>HWND</b>

A handle to the window.

### -param fUnknown [in]

Type: <b>BOOL</b>

A <b>TRUE</b> for this parameter indicates that the window
				is being switched to using the Alt/Ctl+Tab key sequence.  This parameter
				should be <b>FALSE</b> otherwise.

## -remarks

This function is typically called to maintain window z-ordering. 

This function was not included in the SDK headers and libraries until Windows XP with Service Pack 1 (SP1) and Windows Server 2003. If you do not have a header file and import library for this function, you can call the function using <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-iswindowvisible">IsWindowVisible</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-showwindow">ShowWindow</a>



<a href="/windows/desktop/winmsg/windows">Windows</a>
