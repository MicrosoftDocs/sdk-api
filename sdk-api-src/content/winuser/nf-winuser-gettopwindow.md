---
UID: NF:winuser.GetTopWindow
title: GetTopWindow function (winuser.h)
author: windows-sdk-content
description: Examines the Z order of the child windows associated with the specified parent window and retrieves a handle to the child window at the top of the Z order.
old-location: winmsg\gettopwindow.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\gettopwindow.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetTopWindow, GetTopWindow function [Windows and Messages], _win32_GetTopWindow, _win32_gettopwindow_cpp, winmsg.gettopwindow, winui._win32_gettopwindow, winuser/GetTopWindow
ms.topic: function
f1_keywords: 
 - "winuser/GetTopWindow"
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
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
api_name:
 - GetTopWindow
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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

If the function succeeds, the return value is a handle to the child window at the top of the Z order. If the specified window has no child windows, the return value is <b>NULL</b>. To get extended error information, use the <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function. 




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getnextwindow">GetNextWindow</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getwindow">GetWindow</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/winmsg/windows">Windows</a>
 

 

