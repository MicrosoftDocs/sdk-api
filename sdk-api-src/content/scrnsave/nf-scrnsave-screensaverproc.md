---
UID: NF:scrnsave.ScreenSaverProc
title: ScreenSaverProc function (scrnsave.h)
description: Receives messages sent to the specified screen saver window.
helpviewer_keywords: ["ScreenSaverProc","ScreenSaverProc function [Windows Shell]","_win32_ScreenSaverProc","scrnsave/ScreenSaverProc","shell.ScreenSaverProc"]
old-location: shell\ScreenSaverProc.htm
tech.root: shell
ms.assetid: cc013841-41fc-404a-a239-4118f70542b5
ms.date: 12/05/2018
ms.keywords: ScreenSaverProc, ScreenSaverProc function [Windows Shell], _win32_ScreenSaverProc, scrnsave/ScreenSaverProc, shell.ScreenSaverProc
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
req.lib: Scrnsave.lib
req.dll: None
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ScreenSaverProc
 - scrnsave/ScreenSaverProc
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - None
api_name:
 - ScreenSaverProc
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

A screen saver's <b>ScreenSaverProc</b> window procedure should use the <a href="/windows/desktop/api/scrnsave/nf-scrnsave-defscreensaverproc">DefScreenSaverProc</a> function instead of the <a href="/windows/desktop/api/winuser/nf-winuser-defwindowproca">DefWindowProc</a> function to provide default message processing. The <b>DefScreenSaverProc</b> function passes any messages that do not affect screen saver operations to <b>DefWindowProc</b>.

The <b>ScreenSaverProc</b> function must be exported by including it in the EXPORTS statement in the application's module-definition (.def) file.