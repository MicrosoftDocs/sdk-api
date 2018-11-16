---
UID: NF:winuser.IsWindow
title: IsWindow function
author: windows-sdk-content
description: Determines whether the specified window handle identifies an existing window.
old-location: winmsg\iswindow.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\iswindow.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IsWindow, IsWindow function [Windows and Messages], _win32_IsWindow, _win32_iswindow_cpp, winmsg.iswindow, winui._win32_iswindow, winuser/IsWindow
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
 - Ext-MS-Win-NTUser-Window-l1-1-0.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - IsWindow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- IsWindow
: 
---

# IsWindow function


## -description


Determines whether the specified window handle identifies an existing window. 


## -parameters




### -param hWnd [in, optional]

Type: <b>HWND</b>

A handle to the window to be tested. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the window handle identifies an existing window, the return value is nonzero.

If the window handle does not identify an existing window, the return value is zero. 




## -remarks



A thread should not use <b>IsWindow</b> for a window that it did not create because the window could be destroyed after this function was called. Further, because window handles are recycled the handle could even point to a different window. 


#### Examples

For an example, see <a href="https://msdn.microsoft.com/8a5b6bdd-4429-4f48-b846-6bd617a87abf">Creating a Modeless Dialog Box</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/a4001dd3-1534-4a36-bc12-4631a265a77b">IsWindowEnabled</a>



<a href="https://msdn.microsoft.com/6d64e6c4-80b3-48c1-bd1b-00eb3bbbcf4d">IsWindowVisible</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/e2c778c7-7319-4bf7-a6a7-b526e4f3e98b">Windows</a>
 

 

