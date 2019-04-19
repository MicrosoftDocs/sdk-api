---
UID: NF:winuser.GetProcessDefaultLayout
title: GetProcessDefaultLayout function (winuser.h)
author: windows-sdk-content
description: Retrieves the default layout that is used when windows are created with no parent or owner.
old-location: winmsg\getprocessdefaultlayout.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\getprocessdefaultlayout.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetProcessDefaultLayout, GetProcessDefaultLayout function [Windows and Messages], _win32_GetProcessDefaultLayout, _win32_getprocessdefaultlayout_cpp, winmsg.getprocessdefaultlayout, winui._win32_getprocessdefaultlayout, winuser/GetProcessDefaultLayout
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
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - GetProcessDefaultLayout
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetProcessDefaultLayout function


## -description


Retrieves the default layout that is used when windows are created with no parent or owner.


## -parameters




### -param pdwDefaultLayout [out]

Type: <b>DWORD*</b>

The current default process layout. For a list of values, see <a href="https://msdn.microsoft.com/en-us/library/ms633542(v=VS.85).aspx">SetProcessDefaultLayout</a>.


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the function succeeds, the return value is nonzero. 

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The layout specifies how text and graphics are laid out in a window; the default is left to right. The <b>GetProcessDefaultLayout</b> function lets you know if the default layout has changed, from using <a href="https://msdn.microsoft.com/en-us/library/ms633542(v=VS.85).aspx">SetProcessDefaultLayout</a>.




## -see-also




<b>Conceptual</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms633542(v=VS.85).aspx">SetProcessDefaultLayout</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632595(v=VS.85).aspx">Windows</a>
 

 

