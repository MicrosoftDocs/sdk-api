---
UID: NF:winuser.GetShellWindow
title: GetShellWindow function
author: windows-sdk-content
description: Retrieves a handle to the Shell's desktop window.
old-location: winmsg\getshellwindow.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\getshellwindow.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetShellWindow, GetShellWindow function [Windows and Messages], _win32_GetShellWindow, _win32_getshellwindow_cpp, winmsg.getshellwindow, winui._win32_getshellwindow, winuser/GetShellWindow
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
 - API-MS-Win-RTCore-NTUser-shell-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-NTUser-Window-l1-1-0.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - Ext-MS-Win-RTCore-NTUser-iam-l1-1-0.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
 - Ext-MS-Win-RTCore-NTUser-Iam-L1-1-1.dll
api_name:
 - GetShellWindow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetShellWindow function


## -description


Retrieves a handle to the Shell's desktop window.


## -parameters






## -returns



Type: <strong>Type: <b>HWND</b>
</strong>

The return value is the handle of the Shell's desktop window. If no Shell process is present, the return value is <b>NULL</b>.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/0a87f941-a1aa-4e97-b509-912373f6d629">GetDesktopWindow</a>



<a href="https://msdn.microsoft.com/837f8d99-abc5-4c7c-a363-3d178e71aea2">GetWindow</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/e2c778c7-7319-4bf7-a6a7-b526e4f3e98b">Windows</a>
 

 

