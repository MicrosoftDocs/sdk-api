---
UID: NF:winuser.SetWindowPlacement
title: SetWindowPlacement function
author: windows-sdk-content
description: Sets the show state and the restored, minimized, and maximized positions of the specified window.
old-location: winmsg\setwindowplacement.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\setwindowplacement.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: SetWindowPlacement, SetWindowPlacement function [Windows and Messages], _win32_SetWindowPlacement, _win32_setwindowplacement_cpp, winmsg.setwindowplacement, winui._win32_setwindowplacement, winuser/SetWindowPlacement
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - SetWindowPlacement
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- SetWindowPlacement
: 
---

# SetWindowPlacement function


## -description


Sets the show state and the restored, minimized, and maximized positions of the specified window. 


## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window. 


### -param lpwndpl [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms632611(v=VS.85).aspx">WINDOWPLACEMENT</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms632611(v=VS.85).aspx">WINDOWPLACEMENT</a> structure that specifies the new show state and window positions.

 Before calling <b>SetWindowPlacement</b>, set the <b>length</b> member of the <a href="https://msdn.microsoft.com/en-us/library/ms632611(v=VS.85).aspx">WINDOWPLACEMENT</a> structure to sizeof(<b>WINDOWPLACEMENT</b>). <b>SetWindowPlacement</b> fails if the <b>length</b> member is not set correctly.


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



If the information specified in <a href="https://msdn.microsoft.com/en-us/library/ms632611(v=VS.85).aspx">WINDOWPLACEMENT</a> would result in a window that is completely off the screen, the system will automatically adjust the coordinates so that the window is visible, taking into account changes in screen resolution and multiple monitor configuration. 

The <b>length</b> member of <a href="https://msdn.microsoft.com/en-us/library/ms632611(v=VS.85).aspx">WINDOWPLACEMENT</a> must be set to <code>sizeof(WINDOWPLACEMENT)</code>. If this member is not set correctly, the function returns <b>FALSE</b>. For additional remarks on the proper use of window placement coordinates, see <b>WINDOWPLACEMENT</b>. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms633518(v=VS.85).aspx">GetWindowPlacement</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms632611(v=VS.85).aspx">WINDOWPLACEMENT</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632595(v=VS.85).aspx">Windows</a>
 

 

