---
UID: NF:winuser.EnumThreadWindows
title: EnumThreadWindows function
author: windows-sdk-content
description: Enumerates all nonchild windows associated with a thread by passing the handle to each window, in turn, to an application-defined callback function.
old-location: winmsg\enumthreadwindows.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\enumthreadwindows.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: EnumThreadWindows, EnumThreadWindows function [Windows and Messages], _win32_EnumThreadWindows, _win32_enumthreadwindows_cpp, winmsg.enumthreadwindows, winui._win32_enumthreadwindows, winuser/EnumThreadWindows
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.redist: 
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
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - minuser.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - EnumThreadWindows
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# EnumThreadWindows function


## -description


Enumerates all nonchild windows associated with a thread by passing the handle to each window, in turn, to an application-defined callback function. <b>EnumThreadWindows</b> continues until the last window is enumerated or the callback function returns <b>FALSE</b>. To enumerate child windows of a particular window, use the <a href="https://msdn.microsoft.com/en-us/library/ms633494(v=VS.85).aspx">EnumChildWindows</a> function. 


## -parameters




### -param dwThreadId [in]

Type: <b>DWORD</b>

The identifier of the thread whose windows are to be enumerated. 


### -param lpfn [in]

Type: <b>WNDENUMPROC</b>

A pointer to an application-defined callback function. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms633496(v=VS.85).aspx">EnumThreadWndProc</a>. 


### -param lParam [in]

Type: <b>LPARAM</b>

An application-defined value to be passed to the callback function. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the callback function returns <b>TRUE</b> for all windows in the thread specified by <i>dwThreadId</i>, the return value is <b>TRUE</b>. If the callback function returns <b>FALSE</b> on any enumerated window, or if there are no windows found in the thread specified by <i>dwThreadId</i>, the return value is <b>FALSE</b>.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms633494(v=VS.85).aspx">EnumChildWindows</a>



<a href="https://msdn.microsoft.com/en-us/library/ms633496(v=VS.85).aspx">EnumThreadWndProc</a>



<a href="https://msdn.microsoft.com/en-us/library/ms633497(v=VS.85).aspx">EnumWindows</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms632595(v=VS.85).aspx">Windows</a>
 

 

