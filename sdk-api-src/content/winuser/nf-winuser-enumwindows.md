---
UID: NF:winuser.EnumWindows
title: EnumWindows function
author: windows-sdk-content
description: Enumerates all top-level windows on the screen by passing the handle to each window, in turn, to an application-defined callback function. EnumWindows continues until the last top-level window is enumerated or the callback function returns FALSE.
old-location: winmsg\enumwindows.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\enumwindows.htm
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: EnumWindows, EnumWindows function [Windows and Messages], _win32_EnumWindows, _win32_enumwindows_cpp, winmsg.enumwindows, winui._win32_enumwindows, winuser/EnumWindows
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
 - EnumWindows
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# EnumWindows function


## -description


Enumerates all top-level windows on the screen by passing the handle to each window, in turn, to an application-defined callback function. <b>EnumWindows</b> continues until the last top-level window is enumerated or the callback function returns <b>FALSE</b>. 


## -parameters




### -param lpEnumFunc [in]

Type: <b>WNDENUMPROC</b>

A pointer to an application-defined callback function. For more information, see <a href="https://msdn.microsoft.com/library/ms633498(v=VS.85).aspx">EnumWindowsProc</a>. 


### -param lParam [in]

Type: <b>LPARAM</b>

An application-defined value to be passed to the callback function. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

If <a href="https://msdn.microsoft.com/library/ms633498(v=VS.85).aspx">EnumWindowsProc</a> returns zero, the return value is also zero. In this case, the callback function should call <a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a> to obtain a meaningful error code to be returned to the caller of <b>EnumWindows</b>.




## -remarks



The <b>EnumWindows</b> function does not enumerate child windows, with the exception of a few top-level windows owned by the system that have the <b>WS_CHILD</b> style.

This function is more reliable than calling the <a href="https://msdn.microsoft.com/library/ms633515(v=VS.85).aspx">GetWindow</a> function in a loop. An application that calls <b>GetWindow</b> to perform this task risks being caught in an infinite loop or referencing a handle to a window that has been destroyed. 

<div class="alert"><b>Note</b>  For Windows 8 and later, <b>EnumWindows</b> enumerates only top-level windows of desktop apps.</div>
<div> </div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/library/ms633494(v=VS.85).aspx">EnumChildWindows</a>



<a href="https://msdn.microsoft.com/library/ms633498(v=VS.85).aspx">EnumWindowsProc</a>



<a href="https://msdn.microsoft.com/library/ms633515(v=VS.85).aspx">GetWindow</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt637455">Windows</a>
 

 

