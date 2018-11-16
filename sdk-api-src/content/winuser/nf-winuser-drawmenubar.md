---
UID: NF:winuser.DrawMenuBar
title: DrawMenuBar function
author: windows-sdk-content
description: Redraws the menu bar of the specified window. If the menu bar changes after the system has created the window, this function must be called to draw the changed menu bar.
old-location: menurc\drawmenubar.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\drawmenubar.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: DrawMenuBar, DrawMenuBar function [Menus and Other Resources], _win32_DrawMenuBar, _win32_drawmenubar_cpp, menurc.drawmenubar, winui._win32_drawmenubar, winuser/DrawMenuBar
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
api_name:
 - DrawMenuBar
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- DrawMenuBar
: 
---

# DrawMenuBar function


## -description


Redraws the menu bar of the specified window. If the menu bar changes after the system has created the window, this function must be called to draw the changed menu bar. 


## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window whose menu bar is to be redrawn. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms647629(v=VS.85).aspx">DeleteMenu</a>



<a href="https://msdn.microsoft.com/en-us/library/ms647988(v=VS.85).aspx">InsertMenuItem</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646977(v=VS.85).aspx">Menus</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms647994(v=VS.85).aspx">RemoveMenu</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648001(v=VS.85).aspx">SetMenuItemInfo</a>
 

 

