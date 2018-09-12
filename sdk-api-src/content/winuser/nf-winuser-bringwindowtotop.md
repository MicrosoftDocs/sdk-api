---
UID: NF:winuser.BringWindowToTop
title: BringWindowToTop function
author: windows-sdk-content
description: Brings the specified window to the top of the Z order. If the window is a top-level window, it is activated. If the window is a child window, the top-level parent window associated with the child window is activated.
old-location: winmsg\bringwindowtotop.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\bringwindowtotop.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: BringWindowToTop, BringWindowToTop function [Windows and Messages], _win32_BringWindowToTop, _win32_bringwindowtotop_cpp, winmsg.bringwindowtotop, winui._win32_bringwindowtotop, winuser/BringWindowToTop
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
 - Ext-MS-Win-NTUser-Window-l1-1-0.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - BringWindowToTop
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# BringWindowToTop function


## -description


Brings the specified window to the top of the Z order. If the window is a top-level window, it is activated. If the window is a child window, the top-level parent window associated with the child window is activated. 


## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window to bring to the top of the Z order.


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



Use the <b>BringWindowToTop</b> function to uncover any window that is partially or completely obscured by other windows. 

Calling this function is similar to calling the <a href="https://msdn.microsoft.com/en-us/library/ms633545(v=VS.85).aspx">SetWindowPos</a> function to change a window's position in the Z order. <b>BringWindowToTop</b> does not make a window a top-level window. 




## -see-also




<b>Conceptual</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms633545(v=VS.85).aspx">SetWindowPos</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632595(v=VS.85).aspx">Windows</a>
 

 

