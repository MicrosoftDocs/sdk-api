---
UID: NF:winuser.ShowWindowAsync
title: ShowWindowAsync function
author: windows-sdk-content
description: Sets the show state of a window without waiting for the operation to complete.
old-location: winmsg\showwindowasync.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\showwindowasync.htm
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: ShowWindowAsync, ShowWindowAsync function [Windows and Messages], _win32_ShowWindowAsync, _win32_showwindowasync_cpp, winmsg.showwindowasync, winui._win32_showwindowasync, winuser/ShowWindowAsync
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - ShowWindowAsync
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ShowWindowAsync function


## -description


Sets the show state of a window without waiting for the operation to complete. 


## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window. 


### -param nCmdShow [in]

Type: <b>int</b>

Controls how the window is to be shown. For a list of possible values, see the description of the <a href="https://msdn.microsoft.com/13ffef63-3e29-4ca7-a14d-48ff901d82b5">ShowWindow</a> function. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the operation was successfully started, the return value is nonzero. 




## -remarks



This function posts a show-window event to the message queue of the given window. An application can use this function to avoid becoming nonresponsive while waiting for a nonresponsive application to finish processing a show-window event.




## -see-also




<b>Conceptual</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/13ffef63-3e29-4ca7-a14d-48ff901d82b5">ShowWindow</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt637455">Windows</a>
 

 

