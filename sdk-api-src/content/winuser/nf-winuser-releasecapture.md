---
UID: NF:winuser.ReleaseCapture
title: ReleaseCapture function
author: windows-sdk-content
description: Releases the mouse capture from a window in the current thread and restores normal mouse input processing.
old-location: inputdev\releasecapture.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\mouseinput\mouseinputreference\mouseinputfunctions\releasecapture.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ReleaseCapture, ReleaseCapture function [Keyboard and Mouse Input], _win32_ReleaseCapture, _win32_releasecapture_cpp, inputdev.releasecapture, winui._win32_releasecapture, winuser/ReleaseCapture
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
 - Ext-MS-Win-NTUser-mouse-l1-1-0.dll
 - api-ms-win-ntuser-ie-mouse-l1-1-0.dll
 - ie_stubs.dll
api_name:
 - ReleaseCapture
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ReleaseCapture function


## -description


Releases the mouse capture from a window in the current thread and restores normal mouse input processing. A window that has captured the mouse receives all mouse input, regardless of the position of the cursor, except when a mouse button is clicked while the cursor hot spot is in the window of another thread. 


## -parameters






## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.





## -remarks



An application calls this function after calling the <a href="https://msdn.microsoft.com/en-us/library/ms646262(v=VS.85).aspx">SetCapture</a> function. 


#### Examples

For an example, see <a href="https://msdn.microsoft.com/en-us/library/ms645602(v=VS.85).aspx">Drawing Lines with the Mouse</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms646257(v=VS.85).aspx">GetCapture</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645533(v=VS.85).aspx">Mouse Input</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms646262(v=VS.85).aspx">SetCapture</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645605(v=VS.85).aspx">WM_CAPTURECHANGED</a>
 

 

