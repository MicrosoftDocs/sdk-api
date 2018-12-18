---
UID: NF:winuser.IsHungAppWindow
title: IsHungAppWindow function
author: windows-sdk-content
description: Determines whether the system considers that a specified application is not responding.
old-location: winmsg\ishungappwindow.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\ishungappwindow.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IsHungAppWindow, IsHungAppWindow function [Windows and Messages], _win32_IsHungAppWindow, _win32_ishungappwindow_cpp, winmsg.ishungappwindow, winui._win32_ishungappwindow, winuser/IsHungAppWindow
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
 - IsHungAppWindow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IsHungAppWindow function


## -description


<p class="CCE_Message">[This function is not intended for general
      use. It may
      be altered or unavailable in subsequent versions of Windows.]

Determines whether the system considers that a specified application is not responding.
		An application is considered to be not responding if it is not waiting for input, is not in
		startup processing, and has not called <a href="https://msdn.microsoft.com/en-us/library/ms644943(v=VS.85).aspx">PeekMessage</a> within
		the internal timeout period of 5 seconds. 


## -parameters




### -param hwnd [in]

Type: <b>HWND</b>

A handle to the window to be tested. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

The return value is <b>TRUE</b> if the window stops responding; otherwise, it is <b>FALSE</b>.  Ghost windows always return
        <b>TRUE</b>. 




## -remarks



The Windows timeout criteria of 5 seconds is subject to change.

This function was not included in the SDK headers and libraries until Windows XP Service Pack 1 (SP1) and Windows Server 2003. If you do not have a header file and import library for this function, you can call the function using <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a>.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms633528(v=VS.85).aspx">IsWindow</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms632595(v=VS.85).aspx">Windows</a>
 

 

