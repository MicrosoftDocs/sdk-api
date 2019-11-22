---
UID: NS:winuser.tagWINDOWINFO
title: WINDOWINFO (winuser.h)

description: Contains window information.
old-location: winmsg\windowinfo.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowstructures\windowinfo.htm

ms.date: 12/05/2018
ms.keywords: "*LPWINDOWINFO, *PWINDOWINFO, LPWINDOWINFO, LPWINDOWINFO structure pointer [Windows and Messages], PWINDOWINFO, PWINDOWINFO structure pointer [Windows and Messages], WINDOWINFO, WINDOWINFO structure [Windows and Messages], _win32_WINDOWINFO_str, _win32_windowinfo_str_cpp, winmsg.windowinfo, winui._win32_windowinfo_str, winuser/LPWINDOWINFO, winuser/PWINDOWINFO, winuser/WINDOWINFO"
ms.topic: struct
f1_keywords: 
 - "winuser/WINDOWINFO"
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
targetos: Windows
req.typenames: WINDOWINFO, *PWINDOWINFO, *LPWINDOWINFO
req.redist: 
ms.custom: 19H1
---

# WINDOWINFO structure


## -description


Contains window information.


## -struct-fields




### -field cbSize

Type: <b>DWORD</b>

The size of the structure, in bytes. The caller must set this member to <code>sizeof(WINDOWINFO)</code>. 


### -field rcWindow

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a></b>

The coordinates of the window. 


### -field rcClient

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a></b>

The coordinates of the client area. 


### -field dwStyle

Type: <b>DWORD</b>

The window styles. For a table of window styles, see <a href="https://docs.microsoft.com/windows/desktop/winmsg/window-styles">Window Styles</a>. 


### -field dwExStyle

Type: <b>DWORD</b>

The extended window styles. For a table of extended window styles, see <a href="https://docs.microsoft.com/windows/desktop/winmsg/extended-window-styles">Extended Window Styles</a>. 


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

The window class atom (see <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-registerclassa">RegisterClass</a>). 


### -field wCreatorVersion

Type: <b>WORD</b>

The Windows version of the application that created the window. 


## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-createwindowexa">CreateWindowEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getwindowinfo">GetWindowInfo</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-registerclassa">RegisterClass</a>



<a href="https://docs.microsoft.com/windows/desktop/winmsg/windows">Windows</a>
 

 

