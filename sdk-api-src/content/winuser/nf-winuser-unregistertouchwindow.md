---
UID: NF:winuser.UnregisterTouchWindow
title: UnregisterTouchWindow function (winuser.h)
description: Registers a window as no longer being touch-capable.
helpviewer_keywords: ["UnregisterTouchWindow","UnregisterTouchWindow function [Windows Touch]","wintouch.unregistertouchwindow","winuser/UnregisterTouchWindow"]
old-location: wintouch\unregistertouchwindow.htm
tech.root: wintouch
ms.assetid: 19b83312-b52b-45a5-9595-23d4621c4342
ms.date: 12/05/2018
ms.keywords: UnregisterTouchWindow, UnregisterTouchWindow function [Windows Touch], wintouch.unregistertouchwindow, winuser/UnregisterTouchWindow
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UnregisterTouchWindow
 - winuser/UnregisterTouchWindow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - user32.dll
api_name:
 - UnregisterTouchWindow
---

# UnregisterTouchWindow function


## -description

Registers a window as no longer being touch-capable.

## -parameters

### -param hwnd [in]

The handle of the window. The function fails with <b>ERROR_ACCESS_DENIED</b> if the calling thread does not own the specified window.

## -returns

If the function succeeds, the return value is nonzero.
     



If the function fails, the return value is zero. To get extended error information, use the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -remarks

The <b>UnregisterTouchWindow</b>  function succeeds even if the specified window was not previously registered as being touch-capable.

## -see-also

<a href="/windows/desktop/wintouch/mtfunctions">Functions</a>



<a href="/windows/desktop/api/winuser/nf-winuser-registertouchwindow">RegisterTouchWindow</a>