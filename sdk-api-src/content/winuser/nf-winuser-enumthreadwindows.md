---
UID: NF:winuser.EnumThreadWindows
title: EnumThreadWindows function
author: windows-sdk-content
description: Enumerates all nonchild windows associated with a thread by passing the handle to each window, in turn, to an application-defined callback function.
old-location: winmsg\enumthreadwindows.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\enumthreadwindows.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: EnumThreadWindows, EnumThreadWindows function [Windows and Messages], _win32_EnumThreadWindows, _win32_enumthreadwindows_cpp, winmsg.enumthreadwindows, winui._win32_enumthreadwindows, winuser/EnumThreadWindows
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
req.typenames: 
req.redist: 
---

# EnumThreadWindows function


## -description


Enumerates all nonchild windows associated with a thread by passing the handle to each window, in turn, to an application-defined callback function. <b>EnumThreadWindows</b> continues until the last window is enumerated or the callback function returns <b>FALSE</b>. To enumerate child windows of a particular window, use the <a href="https://msdn.microsoft.com/19c4ae31-991c-4b8f-9dfa-eb6cdf4328d8">EnumChildWindows</a> function. 


## -parameters




### -param dwThreadId [in]

Type: <b>DWORD</b>

The identifier of the thread whose windows are to be enumerated. 


### -param lpfn [in]

Type: <b>WNDENUMPROC</b>

A pointer to an application-defined callback function. For more information, see <a href="https://msdn.microsoft.com/50bb90ea-9922-4bbd-8a05-b4bc5b363e20">EnumThreadWndProc</a>. 


### -param lParam [in]

Type: <b>LPARAM</b>

An application-defined value to be passed to the callback function. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the callback function returns <b>TRUE</b> for all windows in the thread specified by <i>dwThreadId</i>, the return value is <b>TRUE</b>. If the callback function returns <b>FALSE</b> on any enumerated window, or if there are no windows found in the thread specified by <i>dwThreadId</i>, the return value is <b>FALSE</b>.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/19c4ae31-991c-4b8f-9dfa-eb6cdf4328d8">EnumChildWindows</a>



<a href="https://msdn.microsoft.com/50bb90ea-9922-4bbd-8a05-b4bc5b363e20">EnumThreadWndProc</a>



<a href="https://msdn.microsoft.com/c4a063ea-a12f-49fe-8654-987e175452a8">EnumWindows</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/e2c778c7-7319-4bf7-a6a7-b526e4f3e98b">Windows</a>
 

 

