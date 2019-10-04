---
UID: NF:winuser.SetWindowDisplayAffinity
title: SetWindowDisplayAffinity function (winuser.h)
author: windows-sdk-content
description: Stores the display affinity setting in kernel mode on the hWnd associated with the window.
old-location: winmsg\setwindowdisplayaffinity.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\setwindowdisplayaffinity.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SetWindowDisplayAffinity, SetWindowDisplayAffinity function [Windows and Messages], _win32_SetWindowDisplayAffinity, _win32_setwindowdisplayaffinity_cpp, winmsg.setwindowdisplayaffinity, winui._win32_setwindowdisplayaffinity, winuser/SetWindowDisplayAffinity
ms.topic: function
f1_keywords: 
 - "winuser/SetWindowDisplayAffinity"
dev_langs:
 - c++
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
 - SetWindowDisplayAffinity
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetWindowDisplayAffinity function


## -description


Stores the display affinity setting in kernel mode on the hWnd associated with the window. 


## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window. 


### -param dwAffinity [in]

Type: <b>DWORD</b>

The display affinity setting. This setting specifies where the window's 
				contents are can be displayed. Set this value to WDA_MONITOR to display the window's contents only on a monitor.
 				
				
				Set this value to WDA_NONE to remove the monitor-only affinity.


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the function succeeds, it returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b> when, for example,  the function call is made on a non top-level window. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. 




## -remarks



This function and <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getwindowdisplayaffinity">GetWindowDisplayAffinity</a> are designed to support the window content protection feature that is new to Windows 7. This feature enables applications to protect their
		own onscreen window content from being captured or copied through a specific set of public operating system features 
		and APIs. However, it works only when the Desktop Window Manager(DWM) is composing the desktop. 
		

It is important to note that unlike a security feature or an implementation of Digital Rights Management (DRM), there is no guarantee that 
		 using <b>SetWindowDisplayAffinity</b> 
		and <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getwindowdisplayaffinity">GetWindowDisplayAffinity</a>, and other necessary functions such as <a href="https://docs.microsoft.com/windows/desktop/api/dwmapi/nf-dwmapi-dwmiscompositionenabled">DwmIsCompositionEnabled</a>, will strictly protect windowed content, for example where someone takes a photograph of the screen.




## -see-also




<b>Conceptual</b>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setwindowdisplayaffinity">SetWindowDisplayAffinity</a>



<a href="https://docs.microsoft.com/windows/desktop/winmsg/windows">Windows</a>
 

 

