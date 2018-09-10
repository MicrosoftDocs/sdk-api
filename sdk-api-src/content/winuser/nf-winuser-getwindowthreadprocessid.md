---
UID: NF:winuser.GetWindowThreadProcessId
title: GetWindowThreadProcessId function
author: windows-sdk-content
description: Retrieves the identifier of the thread that created the specified window and, optionally, the identifier of the process that created the window.
old-location: winmsg\getwindowthreadprocessid.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\getwindowthreadprocessid.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetWindowThreadProcessId, GetWindowThreadProcessId function [Windows and Messages], _win32_GetWindowThreadProcessId, _win32_getwindowthreadprocessid_cpp, winmsg.getwindowthreadprocessid, winui._win32_getwindowthreadprocessid, winuser/GetWindowThreadProcessId
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
 - GetWindowThreadProcessId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetWindowThreadProcessId function


## -description


Retrieves the identifier of the thread that created the specified window and, optionally, the identifier of the process that created the window. 


## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window. 


### -param lpdwProcessId [out, optional]

Type: <b>LPDWORD</b>

A pointer to a variable that receives the process identifier. If this parameter is not <b>NULL</b>, <b>GetWindowThreadProcessId</b> copies the identifier of the process to the variable; otherwise, it does not. 


## -returns



Type: <strong>Type: <b>DWORD</b>
</strong>

The return value is the identifier of the thread that created the window. 




## -see-also




<a href="https://msdn.microsoft.com/e2c778c7-7319-4bf7-a6a7-b526e4f3e98b">Windows Overview</a>
 

 

