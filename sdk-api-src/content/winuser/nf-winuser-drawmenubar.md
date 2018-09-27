---
UID: NF:winuser.DrawMenuBar
title: DrawMenuBar function
author: windows-sdk-content
description: Redraws the menu bar of the specified window. If the menu bar changes after the system has created the window, this function must be called to draw the changed menu bar.
old-location: menurc\drawmenubar.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\drawmenubar.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
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



<a href="https://msdn.microsoft.com/0054bf62-cb70-4d6e-805d-58206fa2d297">DeleteMenu</a>



<a href="https://msdn.microsoft.com/be3819c2-8bdc-4a90-a188-ff8b4060eb8f">InsertMenuItem</a>



<a href="https://msdn.microsoft.com/f00c0b76-fabb-4451-bd4e-30b465d4d235">Menus</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/9557d6dd-44a2-4c26-b939-8ae88b48956a">RemoveMenu</a>



<a href="https://msdn.microsoft.com/e1c669c7-7b56-428a-8433-d926330e42e1">SetMenuItemInfo</a>
 

 

