---
UID: NF:commctrl.MenuHelp
title: MenuHelp function
author: windows-sdk-content
description: Processes WM_MENUSELECT and WM_COMMAND messages and displays Help text about the current menu in the specified status window.
old-location: controls\MenuHelp.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\status\functions\menuhelp.htm
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: MenuHelp, MenuHelp function [Windows Controls], _win32_MenuHelp, _win32_MenuHelp_cpp, commctrl/MenuHelp, controls.MenuHelp, controls._win32_MenuHelp
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Comctl32.lib
req.dll: Comctl32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - MenuHelp
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MenuHelp function


## -description


Processes <a href="https://msdn.microsoft.com/en-us/library/ms646352(v=VS.85).aspx">WM_MENUSELECT</a> and <a href="https://msdn.microsoft.com/en-us/library/ms647591(v=VS.85).aspx">WM_COMMAND</a> messages and displays Help text about the current menu in the specified status window.


## -parameters




### -param uMsg

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Message being processed. This can be either <a href="https://msdn.microsoft.com/en-us/library/ms646352(v=VS.85).aspx">WM_MENUSELECT</a> or <a href="https://msdn.microsoft.com/en-us/library/ms647591(v=VS.85).aspx">WM_COMMAND</a>. 


### -param wParam

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">WPARAM</a></b>

wParam of the message specified in 
					<i>uMsg</i>. 


### -param lParam

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">LPARAM</a></b>

lParam of the message specified in 
					<i>uMsg</i>. 


### -param hMainMenu

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HMENU</a></b>

Handle to the application's main menu. 


### -param hInst

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HINSTANCE</a></b>

Handle to the module that contains the string resources. 


### -param hwndStatus

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the status window. 


### -param lpwIDs

Type: <b>LPUINT</b>

Pointer to an array of values that contains pairs of string resource identifiers and menu handles. The function searches the array for the handle to the selected menu and, if found, uses the corresponding resource identifier to load the appropriate Help string. 


## -returns



No return value.




## -remarks



The <b>MenuHelp</b> function is a helper function. Helper functions are available as a convenience to programming. They combine into one call a sequence of frequently used calls. You use <b>MenuHelp</b> to send <a href="https://msdn.microsoft.com/en-us/library/ms646352(v=VS.85).aspx">WM_MENUSELECT</a> and <a href="https://msdn.microsoft.com/en-us/library/ms647591(v=VS.85).aspx">WM_COMMAND</a> messages.
		



