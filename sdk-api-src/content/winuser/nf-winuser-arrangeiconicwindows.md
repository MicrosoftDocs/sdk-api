---
UID: NF:winuser.ArrangeIconicWindows
title: ArrangeIconicWindows function
author: windows-sdk-content
description: Arranges all the minimized (iconic) child windows of the specified parent window.
old-location: winmsg\arrangeiconicwindows.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\arrangeiconicwindows.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ArrangeIconicWindows, ArrangeIconicWindows function [Windows and Messages], _win32_ArrangeIconicWindows, _win32_arrangeiconicwindows_cpp, winmsg.arrangeiconicwindows, winui._win32_arrangeiconicwindows, winuser/ArrangeIconicWindows
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
 - ArrangeIconicWindows
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- ArrangeIconicWindows
: 
---

# ArrangeIconicWindows function


## -description


Arranges all the minimized (iconic) child windows of the specified parent window. 


## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the parent window.


## -returns



Type: <strong>Type: <b>UINT</b>
</strong>

If the function succeeds, the return value is the height of one row of icons. 

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



An application that maintains its own minimized child windows can use the <b>ArrangeIconicWindows</b> function to arrange icons in a parent window. This function can also arrange icons on the desktop. To retrieve the window handle to the desktop window, use the <a href="https://msdn.microsoft.com/en-us/library/ms633504(v=VS.85).aspx">GetDesktopWindow</a> function. 

An application sends the <a href="https://msdn.microsoft.com/en-us/library/ms644916(v=VS.85).aspx">WM_MDIICONARRANGE</a> message to the multiple-document interface (MDI) client window to prompt the client window to arrange its minimized MDI child windows. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms632678(v=VS.85).aspx">CloseWindow</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms633504(v=VS.85).aspx">GetDesktopWindow</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms632595(v=VS.85).aspx">Windows</a>
 

 

