---
UID: NF:winuser.IsIconic
title: IsIconic function
author: windows-sdk-content
description: Determines whether the specified window is minimized (iconic).
old-location: winmsg\isiconic.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\isiconic.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IsIconic, IsIconic function [Windows and Messages], _win32_IsIconic, _win32_isiconic_cpp, winmsg.isiconic, winui._win32_isiconic, winuser/IsIconic
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-Window-l1-1-0.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - IsIconic
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IsIconic function


## -description


Determines whether the specified window is minimized (iconic).


## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window to be tested.


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the window is iconic, the return value is nonzero.

If the window is not iconic, the return value is zero.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms633531(v=VS.85).aspx">IsZoomed</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt637455">Windows</a>
 

 

