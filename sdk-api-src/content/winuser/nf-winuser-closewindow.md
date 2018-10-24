---
UID: NF:winuser.CloseWindow
title: CloseWindow function
author: windows-sdk-content
description: Minimizes (but does not destroy) the specified window.
old-location: winmsg\closewindow.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\closewindow.htm
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: CloseWindow, CloseWindow function [Windows and Messages], _win32_CloseWindow, _win32_closewindow_cpp, winmsg.closewindow, winui._win32_closewindow, winuser/CloseWindow
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
 - CloseWindow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



To destroy a window, an application must use the <a href="https://msdn.microsoft.com/054fa847-7d6e-4c73-bf8c-b75203713b3e">DestroyWindow</a> function. 




## -see-also




<a href="https://msdn.microsoft.com/61cd07de-399a-481c-81af-504f3dfbcaec">ArrangeIconicWindows</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/054fa847-7d6e-4c73-bf8c-b75203713b3e">DestroyWindow</a>



<a href="https://msdn.microsoft.com/a2f0ff67-e625-4f42-9d8f-e81f52c597e8">IsIconic</a>



<a href="https://msdn.microsoft.com/b94d94c9-8584-4734-8b29-86b475688e9d">OpenIcon</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/e2c778c7-7319-4bf7-a6a7-b526e4f3e98b">Windows</a>
 

 

