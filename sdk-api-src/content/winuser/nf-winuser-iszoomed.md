---
UID: NF:winuser.IsZoomed
title: IsZoomed function
author: windows-sdk-content
description: Determines whether a window is maximized.
old-location: winmsg\iszoomed.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\iszoomed.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IsZoomed, IsZoomed function [Windows and Messages], _win32_IsZoomed, _win32_iszoomed_cpp, winmsg.iszoomed, winui._win32_iszoomed, winuser/IsZoomed
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
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - IsZoomed
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IsZoomed function


## -description


Determines whether a window is maximized. 


## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window to be tested. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the window is zoomed, the return value is nonzero.

If the window is not zoomed, the return value is zero. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/a2f0ff67-e625-4f42-9d8f-e81f52c597e8">IsIconic</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/e2c778c7-7319-4bf7-a6a7-b526e4f3e98b">Windows</a>
 

 

