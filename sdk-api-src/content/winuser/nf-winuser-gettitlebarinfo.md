---
UID: NF:winuser.GetTitleBarInfo
title: GetTitleBarInfo function
author: windows-sdk-content
description: Retrieves information about the specified title bar.
old-location: winmsg\gettitlebarinfo.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\gettitlebarinfo.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetTitleBarInfo, GetTitleBarInfo function [Windows and Messages], _win32_GetTitleBarInfo, _win32_gettitlebarinfo_cpp, winmsg.gettitlebarinfo, winui._win32_gettitlebarinfo, winuser/GetTitleBarInfo
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
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - GetTitleBarInfo
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetTitleBarInfo function


## -description


Retrieves information about the specified title bar.


## -parameters




### -param hwnd [in]

Type: <b>HWND</b>

A handle to the title bar whose information is to be retrieved. 


### -param pti [in, out]

Type: <b>PTITLEBARINFO</b>

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms632608(v=VS.85).aspx">TITLEBARINFO</a> structure to receive the information. Note that you must set the <b>cbSize</b> member to <code>sizeof(TITLEBARINFO)</code> before calling this function. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -see-also




<b>Conceptual</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms632608(v=VS.85).aspx">TITLEBARINFO</a>



<a href="https://msdn.microsoft.com/e2c778c7-7319-4bf7-a6a7-b526e4f3e98b">Windows</a>
 

 

