---
UID: NF:winuser.ArrangeIconicWindows
title: ArrangeIconicWindows function (winuser.h)
description: Arranges all the minimized (iconic) child windows of the specified parent window.
helpviewer_keywords: ["ArrangeIconicWindows","ArrangeIconicWindows function [Windows and Messages]","_win32_ArrangeIconicWindows","_win32_arrangeiconicwindows_cpp","winmsg.arrangeiconicwindows","winui._win32_arrangeiconicwindows","winuser/ArrangeIconicWindows"]
old-location: winmsg\arrangeiconicwindows.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\arrangeiconicwindows.htm
ms.date: 12/05/2018
ms.keywords: ArrangeIconicWindows, ArrangeIconicWindows function [Windows and Messages], _win32_ArrangeIconicWindows, _win32_arrangeiconicwindows_cpp, winmsg.arrangeiconicwindows, winui._win32_arrangeiconicwindows, winuser/ArrangeIconicWindows
f1_keywords:
- winuser/ArrangeIconicWindows
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
api_name:
- ArrangeIconicWindows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ArrangeIconicWindows function


## -description


Arranges all the minimized (iconic) child windows of the specified parent window. 


## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the parent window.


## -returns



Type: <b>UINT</b>

If the function succeeds, the return value is the height of one row of icons. 

If the function fails, the return value is zero. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. 




## -remarks



An application that maintains its own minimized child windows can use the <b>ArrangeIconicWindows</b> function to arrange icons in a parent window. This function can also arrange icons on the desktop. To retrieve the window handle to the desktop window, use the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getdesktopwindow">GetDesktopWindow</a> function. 

An application sends the <a href="https://docs.microsoft.com/windows/desktop/winmsg/wm-mdiiconarrange">WM_MDIICONARRANGE</a> message to the multiple-document interface (MDI) client window to prompt the client window to arrange its minimized MDI child windows. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-closewindow">CloseWindow</a>



<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getdesktopwindow">GetDesktopWindow</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/winmsg/windows">Windows</a>
 

 

