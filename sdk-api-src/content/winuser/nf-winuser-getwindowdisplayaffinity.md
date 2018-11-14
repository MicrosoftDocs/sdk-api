---
UID: NF:winuser.GetWindowDisplayAffinity
title: GetWindowDisplayAffinity function
author: windows-sdk-content
description: Retrieves the current display affinity setting, from any process, for a given window.
old-location: winmsg\getwindowdisplayaffinity.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\getwindowdisplayaffinity.htm
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: GetWindowDisplayAffinity, GetWindowDisplayAffinity function [Windows and Messages], _win32_GetWindowDisplayAffinity, _win32_getwindowdisplayaffinity_cpp, winmsg.getwindowdisplayaffinity, winui._win32_getwindowdisplayaffinity, winuser/GetWindowDisplayAffinity
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - GetWindowDisplayAffinity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- GetWindowDisplayAffinity
: 
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

The display affinity setting.
				


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

This function succeeds only when the window is layered and Desktop Windows Manager 
				is composing the desktop. If this function succeeds, it returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>. 
				To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



This function currently only supports one flag, <b>WDA_MONITOR</b> (0x01). This flag  enables  a window's contents to be displayed only on the monitor.
		

This function and <a href="https://msdn.microsoft.com/fb6c50e1-3051-4881-bd94-46c1206ff4ab">SetWindowDisplayAffinity</a> are designed to support the window content protection feature unique to Windows 7. This feature enables applications to protect their
		own onscreen window content from being captured or copied via a specific set of public operating system features 
		and APIs. However, it works only when the Desktop Window Manager (DWM) is composing the desktop. 
		

It is important to note that unlike a security feature or an implementation of Digital Rights Management (DRM), there is no guarantee that 
		 using <a href="https://msdn.microsoft.com/fb6c50e1-3051-4881-bd94-46c1206ff4ab">SetWindowDisplayAffinity</a> 
		and <b>GetWindowDisplayAffinity</b>, and other necessary functions such as <a href="https://msdn.microsoft.com/31edec77-9869-4585-838d-93b2fcab31a5">DwmIsCompositionEnabled</a>, will strictly protect windowed content, as in the case where someone takes a photograph of the screen.
		




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/e2c778c7-7319-4bf7-a6a7-b526e4f3e98b">Windows</a>
 

 

