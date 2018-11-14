---
UID: NF:winuser.WindowFromPoint
title: WindowFromPoint function
author: windows-sdk-content
description: Retrieves a handle to the window that contains the specified point.
old-location: winmsg\windowfrompoint.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\windowfrompoint.htm
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: WindowFromPoint, WindowFromPoint function [Windows and Messages], _win32_WindowFromPoint, _win32_windowfrompoint_cpp, winmsg.windowfrompoint, winui._win32_windowfrompoint, winuser/WindowFromPoint
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
 - WindowFromPoint
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- WindowFromPoint
: 
---

# WindowFromPoint function


## -description


Retrieves a handle to the window that contains the specified point. 


## -parameters




### -param Point [in]

Type: <b><a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a></b>

The point to be checked. 


## -returns



Type: <strong>Type: <b>HWND</b>
</strong>

The return value is a handle to the window that contains the point. If no window exists at the given point, the return value is <b>NULL</b>. If the point is over a static text control, the return value is a handle to the window under the static text control. 




## -remarks



The <b>WindowFromPoint</b> function does not retrieve a handle to a hidden or disabled window, even if the point is within the window. An application should use the <a href="https://msdn.microsoft.com/en-us/library/ms632676(v=VS.85).aspx">ChildWindowFromPoint</a> function for a nonrestrictive search. 


#### Examples

For an example, see "Interface from Running Object Table" in <a href="https://msdn.microsoft.com/en-us/library/Bb787724(v=VS.85).aspx">About Text Object Model</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms632676(v=VS.85).aspx">ChildWindowFromPoint</a>



<b>Conceptual</b>



<b>Other Resources</b>



<a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/57ecec82-03be-4d1a-84cf-6b64131af19d">WindowFromDC</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632595(v=VS.85).aspx">Windows</a>
 

 

