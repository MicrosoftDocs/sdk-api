---
UID: NF:winuser.ShowWindowAsync
title: ShowWindowAsync function (winuser.h)
description: Sets the show state of a window without waiting for the operation to complete.
old-location: winmsg\showwindowasync.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\showwindowasync.htm
ms.date: 12/05/2018
ms.keywords: ShowWindowAsync, ShowWindowAsync function [Windows and Messages], _win32_ShowWindowAsync, _win32_showwindowasync_cpp, winmsg.showwindowasync, winui._win32_showwindowasync, winuser/ShowWindowAsync
f1_keywords:
- winuser/ShowWindowAsync
dev_langs:
- c++
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
- Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
- ShowWindowAsync
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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

Controls how the window is to be shown. For a list of possible values, see the description of the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-showwindow">ShowWindow</a> function. 


## -returns



Type: <b>BOOL</b>

If the operation was successfully started, the return value is nonzero. 




## -remarks



This function posts a show-window event to the message queue of the given window. An application can use this function to avoid becoming nonresponsive while waiting for a nonresponsive application to finish processing a show-window event.




## -see-also




<b>Conceptual</b>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-showwindow">ShowWindow</a>



<a href="https://docs.microsoft.com/windows/desktop/winmsg/windows">Windows</a>
 

 

