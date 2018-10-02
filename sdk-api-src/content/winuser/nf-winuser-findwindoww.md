---
UID: NF:winuser.FindWindowW
title: FindWindowW function
author: windows-sdk-content
description: Retrieves a handle to the top-level window whose class name and window name match the specified strings. This function does not search child windows. This function does not perform a case-sensitive search.
old-location: winmsg\findwindow.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\findwindow.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: FindWindow, FindWindow function [Windows and Messages], FindWindowA, FindWindowW, _win32_FindWindow, _win32_findwindow_cpp, winmsg.findwindow, winui._win32_findwindow, winuser/FindWindow, winuser/FindWindowA, winuser/FindWindowW
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
req.unicode-ansi: FindWindowW (Unicode) and FindWindowA (ANSI)
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
 - FindWindow
 - FindWindowA
 - FindWindowW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FindWindowW function


## -description


Retrieves a handle to the top-level window whose class name and window name match the specified strings. This function does not search child windows. This function does not perform a case-sensitive search.

To search child windows, beginning with a specified child window, use the <a href="https://msdn.microsoft.com/en-us/library/ms633500(v=VS.85).aspx">FindWindowEx</a> function.


## -parameters




### -param lpClassName [in, optional]

Type: <b>LPCTSTR</b>

The class name or a class atom created by a previous call to the <a href="https://msdn.microsoft.com/en-us/library/ms633586(v=VS.85).aspx">RegisterClass</a> or <a href="https://msdn.microsoft.com/en-us/library/ms633587(v=VS.85).aspx">RegisterClassEx</a> function. The atom must be in the low-order word of <i>lpClassName</i>; the high-order word must be zero. 

If <i>lpClassName</i> points to a string, it specifies the window class name. The class name can be any name registered with <a href="https://msdn.microsoft.com/en-us/library/ms633586(v=VS.85).aspx">RegisterClass</a> or <a href="https://msdn.microsoft.com/en-us/library/ms633587(v=VS.85).aspx">RegisterClassEx</a>, or any of the predefined control-class names. 

If <i>lpClassName</i> is <b>NULL</b>, it finds any window whose title matches the <i>lpWindowName</i> parameter. 


### -param lpWindowName [in, optional]

Type: <b>LPCTSTR</b>

The window name (the window's title). If this parameter is <b>NULL</b>, all window names match. 


## -returns



Type: <strong>Type: <b>HWND</b>
</strong>

If the function succeeds, the return value is a handle to the window that has the specified class name and window name.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



If the <i>lpWindowName</i> parameter is not <b>NULL</b>, <b>FindWindow</b> calls the <a href="https://msdn.microsoft.com/en-us/library/ms633520(v=VS.85).aspx">GetWindowText</a> function to retrieve the window name for comparison. For a description of a potential problem that can arise, see the Remarks for <b>GetWindowText</b>. 


#### Examples

For an example, see <a href="https://msdn.microsoft.com/en-us/library/ms645602(v=VS.85).aspx">Retrieving the Number of Mouse Wheel Scroll Lines</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms633497(v=VS.85).aspx">EnumWindows</a>



<a href="https://msdn.microsoft.com/en-us/library/ms633500(v=VS.85).aspx">FindWindowEx</a>



<a href="https://msdn.microsoft.com/en-us/library/ms633582(v=VS.85).aspx">GetClassName</a>



<a href="https://msdn.microsoft.com/en-us/library/ms633520(v=VS.85).aspx">GetWindowText</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms633586(v=VS.85).aspx">RegisterClass</a>



<a href="https://msdn.microsoft.com/en-us/library/ms633587(v=VS.85).aspx">RegisterClassEx</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632595(v=VS.85).aspx">Windows</a>
 

 

