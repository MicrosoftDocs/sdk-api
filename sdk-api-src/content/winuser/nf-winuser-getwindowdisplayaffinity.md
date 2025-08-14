---
UID: NF:winuser.GetWindowDisplayAffinity
title: GetWindowDisplayAffinity function (winuser.h)
description: Retrieves the current display affinity setting, from any process, for a given window.
helpviewer_keywords: ["GetWindowDisplayAffinity","GetWindowDisplayAffinity function [Windows and Messages]","_win32_GetWindowDisplayAffinity","_win32_getwindowdisplayaffinity_cpp","winmsg.getwindowdisplayaffinity","winui._win32_getwindowdisplayaffinity","winuser/GetWindowDisplayAffinity"]
old-location: winmsg\getwindowdisplayaffinity.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\getwindowdisplayaffinity.htm
ms.date: 12/05/2018
ms.keywords: GetWindowDisplayAffinity, GetWindowDisplayAffinity function [Windows and Messages], _win32_GetWindowDisplayAffinity, _win32_getwindowdisplayaffinity_cpp, winmsg.getwindowdisplayaffinity, winui._win32_getwindowdisplayaffinity, winuser/GetWindowDisplayAffinity
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - GetWindowDisplayAffinity
 - winuser/GetWindowDisplayAffinity
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
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - GetWindowDisplayAffinity
req.apiset: ext-ms-win-ntuser-window-l1-1-1 (introduced in Windows 8.1)
---

# GetWindowDisplayAffinity function


## -description

Retrieves the current display affinity setting, from any process, for a given window.

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window.

### -param pdwAffinity [out]

Type: <b>DWORD*</b>

A pointer to a variable that receives the display affinity setting.
See <a href="/windows/desktop/api/winuser/nf-winuser-setwindowdisplayaffinity">SetWindowDisplayAffinity</a> for a list of affinity settings and their meanings.

## -returns

Type: <b>BOOL</b>

This function succeeds only when the window is layered and Desktop Windows Manager 
				is composing the desktop. If this function succeeds, it returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>. 
				To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function and <a href="/windows/desktop/api/winuser/nf-winuser-setwindowdisplayaffinity">SetWindowDisplayAffinity</a> are designed to support the window content protection feature unique to Windows 7. This feature enables applications to protect their
		own onscreen window content from being captured or copied via a specific set of public operating system features 
		and APIs. However, it works only when the Desktop Window Manager (DWM) is composing the desktop. 
		

It is important to note that unlike a security feature or an implementation of Digital Rights Management (DRM), there is no guarantee that 
		 using <a href="/windows/desktop/api/winuser/nf-winuser-setwindowdisplayaffinity">SetWindowDisplayAffinity</a> 
		and <b>GetWindowDisplayAffinity</b>, and other necessary functions such as <a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmiscompositionenabled">DwmIsCompositionEnabled</a>, will strictly protect windowed content, as in the case where someone takes a photograph of the screen.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/winmsg/windows">Windows</a>
