---
UID: NF:winuser.IsWindowVisible
title: IsWindowVisible function
author: windows-sdk-content
description: Determines the visibility state of the specified window.
old-location: winmsg\iswindowvisible.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\iswindowvisible.htm
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IsWindowVisible, IsWindowVisible function [Windows and Messages], _win32_IsWindowVisible, _win32_iswindowvisible_cpp, winmsg.iswindowvisible, winui._win32_iswindowvisible, winuser/IsWindowVisible
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
 - API-MS-Win-NTUser-IE-Window-l1-1-0.dll
 - ie_shims.dll
 - API-MS-Win-RTCore-NTUser-Window-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - IsWindowVisible
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- IsWindowVisible
: 
---

# IsWindowVisible function


## -description


Determines the visibility state of the specified window. 


## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window to be tested. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the specified window, its parent window, its parent's parent window, and so forth, have the <b>WS_VISIBLE</b> style, the return value is nonzero. Otherwise, the return value is zero. 

Because the return value specifies whether the window has the <b>WS_VISIBLE</b> style, it may be nonzero even if the window is totally obscured by other windows. 




## -remarks



The visibility state of a window is indicated by the <b>WS_VISIBLE</b> style bit. When <b>WS_VISIBLE</b> is set, the window is displayed and subsequent drawing into it is displayed as long as the window has the <b>WS_VISIBLE</b> style. 

Any drawing to a window with the <b>WS_VISIBLE</b> style will not be displayed if the window is obscured by other windows or is clipped by its parent window. 




## -see-also




<b>Conceptual</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/13ffef63-3e29-4ca7-a14d-48ff901d82b5">ShowWindow</a>



<a href="https://msdn.microsoft.com/e2c778c7-7319-4bf7-a6a7-b526e4f3e98b">Windows</a>
 

 

