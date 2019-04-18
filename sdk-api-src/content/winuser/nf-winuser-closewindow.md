---
UID: NF:winuser.CloseWindow
title: CloseWindow function (winuser.h)
author: windows-sdk-content
description: Minimizes (but does not destroy) the specified window.
old-location: winmsg\closewindow.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\closewindow.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CloseWindow, CloseWindow function [Windows and Messages], _win32_CloseWindow, _win32_closewindow_cpp, winmsg.closewindow, winui._win32_closewindow, winuser/CloseWindow
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
 - CloseWindow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CloseWindow function


## -description


Minimizes (but does not destroy) the specified window. 


## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window to be minimized. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



To destroy a window, an application must use the <a href="https://msdn.microsoft.com/en-us/library/ms632682(v=VS.85).aspx">DestroyWindow</a> function. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms632671(v=VS.85).aspx">ArrangeIconicWindows</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms632682(v=VS.85).aspx">DestroyWindow</a>



<a href="https://msdn.microsoft.com/en-us/library/ms633527(v=VS.85).aspx">IsIconic</a>



<a href="https://msdn.microsoft.com/en-us/library/ms633535(v=VS.85).aspx">OpenIcon</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms632595(v=VS.85).aspx">Windows</a>
 

 

