---
UID: NF:winuser.FlashWindow
title: FlashWindow function (winuser.h)
description: Flashes the specified window one time. It does not change the active state of the window.
helpviewer_keywords: ["FlashWindow","FlashWindow function","_win32_flashwindow","base.flashwindow","winuser/FlashWindow"]
old-location: base\flashwindow.htm
tech.root: Debug
ms.assetid: c4af997d-5cb8-4d5d-ae8d-1e0cc724fe02
ms.date: 12/05/2018
ms.keywords: FlashWindow, FlashWindow function, _win32_flashwindow, base.flashwindow, winuser/FlashWindow
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - FlashWindow
 - winuser/FlashWindow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-misc-l1-7-0.dll
 - ext-ms-win-ntuser-misc-l1-6-0.dll
 - ext-ms-win-ntuser-misc-l1-5-1.dll
 - ext-ms-win-ntuser-misc-l1-5-0.dll
 - User32.dll
api_name:
 - FlashWindow
---

# FlashWindow function


## -description

Flashes the specified window one time. It does not change the active state of the window.

To flash the window a specified number of times, use the 
<a href="/windows/desktop/api/winuser/nf-winuser-flashwindowex">FlashWindowEx</a> function.

## -parameters

### -param hWnd [in]

A handle to the window to be flashed. The window can be either open or minimized.

### -param bInvert [in]

If this parameter is <b>TRUE</b>, the window is flashed from one state to the other. If it is <b>FALSE</b>, the window is returned to its original state (either active or inactive). 




When an application is minimized and this parameter is <b>TRUE</b>, the taskbar window button flashes active/inactive. If it is <b>FALSE</b>, the taskbar window button flashes inactive, meaning that it does not change colors. It flashes, as if it were being redrawn, but it does not provide the visual invert clue to the user.

## -returns

The return value specifies the window's state before the call to the 
<b>FlashWindow</b> function. If the window caption was drawn as active before the call, the return value is nonzero. Otherwise, the return value is zero.

## -remarks

Flashing a window means changing the appearance of its caption bar as if the window were changing from inactive to active status, or vice versa. (An inactive caption bar changes to an active caption bar; an active caption bar changes to an inactive caption bar.)

Typically, a window is flashed to inform the user that the window requires attention but that it does not currently have the keyboard focus.

The 
<b>FlashWindow</b> function flashes the window only once; for repeated flashing, the application should create a system timer.

## -see-also

<a href="/windows/desktop/Debug/error-handling-functions">Error Handling Functions</a>



<a href="/windows/desktop/Debug/notifying-the-user">Notifying the User</a>