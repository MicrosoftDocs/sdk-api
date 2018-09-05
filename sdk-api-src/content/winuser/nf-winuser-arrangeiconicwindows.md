---
UID: NF:winuser.ArrangeIconicWindows
title: ArrangeIconicWindows function
author: windows-sdk-content
description: Arranges all the minimized (iconic) child windows of the specified parent window.
old-location: winmsg\arrangeiconicwindows.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\arrangeiconicwindows.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ArrangeIconicWindows, ArrangeIconicWindows function [Windows and Messages], _win32_ArrangeIconicWindows, _win32_arrangeiconicwindows_cpp, winmsg.arrangeiconicwindows, winui._win32_arrangeiconicwindows, winuser/ArrangeIconicWindows
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.redist: 
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
api_name:
 - ArrangeIconicWindows
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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



An application that maintains its own minimized child windows can use the <b>ArrangeIconicWindows</b> function to arrange icons in a parent window. This function can also arrange icons on the desktop. To retrieve the window handle to the desktop window, use the <a href="https://msdn.microsoft.com/0a87f941-a1aa-4e97-b509-912373f6d629">GetDesktopWindow</a> function. 

An application sends the <a href="https://msdn.microsoft.com/935b9e29-224d-449e-b89f-b6062bed7702">WM_MDIICONARRANGE</a> message to the multiple-document interface (MDI) client window to prompt the client window to arrange its minimized MDI child windows. 




## -see-also




<a href="https://msdn.microsoft.com/6bb41c24-458a-42ee-9e60-592e20881e06">CloseWindow</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/0a87f941-a1aa-4e97-b509-912373f6d629">GetDesktopWindow</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/e2c778c7-7319-4bf7-a6a7-b526e4f3e98b">Windows</a>
 

 

