---
UID: NF:scrnsave.ScreenSaverProc
title: ScreenSaverProc function
author: windows-sdk-content
description: Receives messages sent to the specified screen saver window.
old-location: shell\ScreenSaverProc.htm
old-project: shell
ms.assetid: cc013841-41fc-404a-a239-4118f70542b5
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: ScreenSaverProc, ScreenSaverProc function [Windows Shell], _win32_ScreenSaverProc, scrnsave/ScreenSaverProc, shell.ScreenSaverProc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: scrnsave.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.typenames: SCHEDULE_HEADER, *PSCHEDULE_HEADER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - None
api_name:
 - ScreenSaverProc
product: Windows
targetos: Windows
req.lib: Scrnsave.lib
req.dll: None
req.irql: 
req.product: ADAM
---

# ScreenSaverProc function


## -description


Receives messages sent to the specified screen saver window.


## -parameters




### -param hWnd

Type: <b>HWND</b>

An identifier of the window.


### -param message

Type: <b>UINT</b>

A message sent to the screen saver window.


### -param wParam

Type: <b>WPARAM</b>

Additional message-specific information.


### -param lParam

Type: <b>LPARAM</b>

Additional message-specific information.


## -returns



Type: <b>LONG</b>

The return value is the result of the message processing and depends on the message sent.




## -remarks



A screen saver's <b>ScreenSaverProc</b> window procedure should use the <a href="https://msdn.microsoft.com/eda5c4d4-0484-4c81-a699-5fedea0bd1c2">DefScreenSaverProc</a> function instead of the <a href="https://msdn.microsoft.com/library/ms633572(v=VS.85).aspx">DefWindowProc</a> function to provide default message processing. The <b>DefScreenSaverProc</b> function passes any messages that do not affect screen saver operations to <b>DefWindowProc</b>.

The <b>ScreenSaverProc</b> function must be exported by including it in the EXPORTS statement in the application's module-definition (.def) file.



