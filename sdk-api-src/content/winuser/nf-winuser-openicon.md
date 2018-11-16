---
UID: NF:winuser.OpenIcon
title: OpenIcon function
author: windows-sdk-content
description: Restores a minimized (iconic) window to its previous size and position; it then activates the window.
old-location: winmsg\openicon.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\openicon.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: OpenIcon, OpenIcon function [Windows and Messages], _win32_OpenIcon, _win32_openicon_cpp, winmsg.openicon, winui._win32_openicon, winuser/OpenIcon
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
api_name:
 - OpenIcon
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- OpenIcon
: 
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



<b>OpenIcon</b> sends a <a href="https://msdn.microsoft.com/en-us/library/ms632640(v=VS.85).aspx">WM_QUERYOPEN</a> message to the given window. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms632678(v=VS.85).aspx">CloseWindow</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms633527(v=VS.85).aspx">IsIconic</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms633548(v=VS.85).aspx">ShowWindow</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632595(v=VS.85).aspx">Windows</a>
 

 

