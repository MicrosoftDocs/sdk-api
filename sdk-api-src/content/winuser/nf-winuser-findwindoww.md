---
UID: NF:winuser.FindWindowW
title: FindWindowW function (winuser.h)
author: windows-sdk-content
description: Retrieves a handle to the top-level window whose class name and window name match the specified strings. This function does not search child windows. This function does not perform a case-sensitive search.
old-location: winmsg\findwindow.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\findwindow.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FindWindow, FindWindow function [Windows and Messages], FindWindowA, FindWindowW, _win32_FindWindow, _win32_findwindow_cpp, winmsg.findwindow, winui._win32_findwindow, winuser/FindWindow, winuser/FindWindowA, winuser/FindWindowW
ms.topic: function
f1_keywords: 
 - "winuser/FindWindow"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FindWindowW function


## -description


Retrieves a handle to the top-level window whose class name and window name match the specified strings. This function does not search child windows. This function does not perform a case-sensitive search.

To search child windows, beginning with a specified child window, use the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-findwindowexa">FindWindowEx</a> function.


## -parameters




### -param lpClassName [in, optional]

Type: <b>LPCTSTR</b>

The class name or a class atom created by a previous call to the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-registerclassa">RegisterClass</a> or <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-registerclassexa">RegisterClassEx</a> function. The atom must be in the low-order word of <i>lpClassName</i>; the high-order word must be zero. 

If <i>lpClassName</i> points to a string, it specifies the window class name. The class name can be any name registered with <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-registerclassa">RegisterClass</a> or <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-registerclassexa">RegisterClassEx</a>, or any of the predefined control-class names. 

If <i>lpClassName</i> is <b>NULL</b>, it finds any window whose title matches the <i>lpWindowName</i> parameter. 


### -param lpWindowName [in, optional]

Type: <b>LPCTSTR</b>

The window name (the window's title). If this parameter is <b>NULL</b>, all window names match. 


## -returns



Type: <strong>Type: <b>HWND</b>
</strong>

If the function succeeds, the return value is a handle to the window that has the specified class name and window name.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. 




## -remarks



If the <i>lpWindowName</i> parameter is not <b>NULL</b>, <b>FindWindow</b> calls the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getwindowtexta">GetWindowText</a> function to retrieve the window name for comparison. For a description of a potential problem that can arise, see the Remarks for <b>GetWindowText</b>. 


#### Examples

For an example, see <a href="https://docs.microsoft.com/windows/desktop/inputdev/using-mouse-input">Retrieving the Number of Mouse Wheel Scroll Lines</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-enumwindows">EnumWindows</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-findwindowexa">FindWindowEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getclassname">GetClassName</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getwindowtexta">GetWindowText</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-registerclassa">RegisterClass</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-registerclassexa">RegisterClassEx</a>



<a href="https://docs.microsoft.com/windows/desktop/winmsg/windows">Windows</a>
 

 

