---
UID: NF:winuser.ShowOwnedPopups
title: ShowOwnedPopups function
author: windows-sdk-content
description: Shows or hides all pop-up windows owned by the specified window.
old-location: winmsg\showownedpopups.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\showownedpopups.htm
ms.author: windowssdkdev
ms.date: 03/29/2018
ms.keywords: ShowOwnedPopups, ShowOwnedPopups function [Windows and Messages], _win32_ShowOwnedPopups, _win32_showownedpopups_cpp, winmsg.showownedpopups, winui._win32_showownedpopups, winuser/ShowOwnedPopups
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: POINTER_DEVICE_TYPE
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
 - ShowOwnedPopups
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ShowOwnedPopups function


## -description


Shows or hides all pop-up windows owned by the specified window. 


## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window that owns the pop-up windows to be shown or hidden. 


### -param fShow [in]

Type: <b>BOOL</b>

If this parameter is <b>TRUE</b>, all hidden pop-up windows are shown. If this parameter is <b>FALSE</b>, all visible pop-up windows are hidden. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



<b>ShowOwnedPopups</b> shows only windows hidden by a previous call to <b>ShowOwnedPopups</b>. For example, if a pop-up window is hidden by using the <a href="https://msdn.microsoft.com/library/ms633548(v=VS.85).aspx">ShowWindow</a> function, subsequently calling <b>ShowOwnedPopups</b> with the <i>fShow</i> parameter set to <b>TRUE</b> does not cause the window to be shown. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/library/ms633530(v=VS.85).aspx">IsWindowVisible</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/library/ms633548(v=VS.85).aspx">ShowWindow</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt637455">Windows</a>
 

 

