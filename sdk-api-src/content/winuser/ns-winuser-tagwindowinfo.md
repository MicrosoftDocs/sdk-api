---
UID: NS:winuser.tagWINDOWINFO
title: tagWINDOWINFO
author: windows-sdk-content
description: Contains window information.
old-location: winmsg\windowinfo.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowstructures\windowinfo.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*LPWINDOWINFO, *PWINDOWINFO, LPWINDOWINFO, LPWINDOWINFO structure pointer [Windows and Messages], PWINDOWINFO, PWINDOWINFO structure pointer [Windows and Messages], WINDOWINFO, WINDOWINFO structure [Windows and Messages], _win32_WINDOWINFO_str, _win32_windowinfo_str_cpp, tagWINDOWINFO, winmsg.windowinfo, winui._win32_windowinfo_str, winuser/LPWINDOWINFO, winuser/PWINDOWINFO, winuser/WINDOWINFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - WINDOWINFO
product: Windows
targetos: Windows
req.typenames: WINDOWINFO, *PWINDOWINFO, *LPWINDOWINFO
req.redist: 
---

# tagWINDOWINFO structure


## -description


Contains window information.


## -struct-fields




### -field cbSize

Type: <b>DWORD</b>

The size of the structure, in bytes. The caller must set this member to <code>sizeof(WINDOWINFO)</code>. 


### -field rcWindow

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a></b>

The coordinates of the window. 


### -field rcClient

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a></b>

The coordinates of the client area. 


### -field dwStyle

Type: <b>DWORD</b>

The window styles. For a table of window styles, see <a href="https://msdn.microsoft.com/en-us/library/ms632600(v=VS.85).aspx">Window Styles</a>. 


### -field dwExStyle

Type: <b>DWORD</b>

The extended window styles. For a table of extended window styles, see <a href="https://msdn.microsoft.com/5830B16E-CD52-4a1a-A1BD-3AFE66BA5FDD">Extended Window Styles</a>. 


### -field dwWindowStatus

Type: <b>DWORD</b>

The window status. If this member is <b>WS_ACTIVECAPTION</b> (0x0001), the window is active. Otherwise, this member is zero. 


### -field cxWindowBorders

Type: <b>UINT</b>

The width of the window border, in pixels. 


### -field cyWindowBorders

Type: <b>UINT</b>

The height of the window border, in pixels. 


### -field atomWindowType

Type: <b>ATOM</b>

The window class atom (see <a href="https://msdn.microsoft.com/en-us/library/ms633586(v=VS.85).aspx">RegisterClass</a>). 


### -field wCreatorVersion

Type: <b>WORD</b>

The Windows version of the application that created the window. 


## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms632680(v=VS.85).aspx">CreateWindowEx</a>



<a href="https://msdn.microsoft.com/en-us/library/ms633516(v=VS.85).aspx">GetWindowInfo</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms633586(v=VS.85).aspx">RegisterClass</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632595(v=VS.85).aspx">Windows</a>
 

 

