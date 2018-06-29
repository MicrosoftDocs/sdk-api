---
UID: NF:winuser.GetTopWindow
title: GetTopWindow function
author: windows-sdk-content
description: Examines the Z order of the child windows associated with the specified parent window and retrieves a handle to the child window at the top of the Z order.
old-location: winmsg\gettopwindow.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\gettopwindow.htm
ms.author: windowssdkdev
ms.date: 03/29/2018
ms.keywords: GetTopWindow, GetTopWindow function [Windows and Messages], _win32_GetTopWindow, _win32_gettopwindow_cpp, winmsg.gettopwindow, winui._win32_gettopwindow, winuser/GetTopWindow
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
req.typenames: POINTER_DEVICE_TYPE
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
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
api_name:
 - GetTopWindow
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetTopWindow function


## -description


Examines the Z order of the child windows associated with the specified parent window and retrieves a handle to the child window at the top of the Z order. 


## -parameters




### -param hWnd [in, optional]

Type: <b>HWND</b>

A handle to the parent window whose child windows are to be examined. If this parameter is <b>NULL</b>, the function returns a handle to the window at the top of the Z order. 


## -returns



Type: <strong>Type: <b>HWND</b>
</strong>

If the function succeeds, the return value is a handle to the child window at the top of the Z order. If the specified window has no child windows, the return value is <b>NULL</b>. To get extended error information, use the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/library/ms633509(v=VS.85).aspx">GetNextWindow</a>



<a href="https://msdn.microsoft.com/library/ms633515(v=VS.85).aspx">GetWindow</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt637455">Windows</a>
 

 

