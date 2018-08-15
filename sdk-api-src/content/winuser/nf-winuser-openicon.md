---
UID: NF:winuser.OpenIcon
title: OpenIcon function
author: windows-sdk-content
description: Restores a minimized (iconic) window to its previous size and position; it then activates the window.
old-location: winmsg\openicon.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\openicon.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: OpenIcon, OpenIcon function [Windows and Messages], _win32_OpenIcon, _win32_openicon_cpp, winmsg.openicon, winui._win32_openicon, winuser/OpenIcon
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
 - OpenIcon
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# OpenIcon function


## -description


Restores a minimized (iconic) window to its previous size and position; it then activates the window. 


## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window to be restored and activated. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



<b>OpenIcon</b> sends a <a href="https://msdn.microsoft.com/6e14d5fd-6598-4d2e-a463-2b153c9c2aa3">WM_QUERYOPEN</a> message to the given window. 




## -see-also




<a href="https://msdn.microsoft.com/6bb41c24-458a-42ee-9e60-592e20881e06">CloseWindow</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/a2f0ff67-e625-4f42-9d8f-e81f52c597e8">IsIconic</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/13ffef63-3e29-4ca7-a14d-48ff901d82b5">ShowWindow</a>



<a href="https://msdn.microsoft.com/e2c778c7-7319-4bf7-a6a7-b526e4f3e98b">Windows</a>
 

 

