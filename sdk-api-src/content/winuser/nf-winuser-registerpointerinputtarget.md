---
UID: NF:winuser.RegisterPointerInputTarget
title: RegisterPointerInputTarget function (winuser.h)
description: Allows the caller to register a target window to which all pointer input of the specified type is redirected.
helpviewer_keywords: ["RegisterPointerInputTarget","RegisterPointerInputTarget function [Windows Accessibility]","inputmsg.registerpointerinputtarget","winauto.RegisterPointerInputTarget","winuser/RegisterPointerInputTarget"]
old-location: winauto\RegisterPointerInputTarget.htm
tech.root: WinAuto
ms.assetid: 75faea24-91cd-448b-b67a-09fe530f1830
ms.date: 12/05/2018
ms.keywords: RegisterPointerInputTarget, RegisterPointerInputTarget function [Windows Accessibility], inputmsg.registerpointerinputtarget, winauto.RegisterPointerInputTarget, winuser/RegisterPointerInputTarget
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - RegisterPointerInputTarget
 - winuser/RegisterPointerInputTarget
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-wmpointermin-l1-1-0.dll
 - api-ms-win-rtcore-ntuser-wmpointer-l1-2-0.dll
 - User32.dll
 - API-MS-Win-RTCore-NTUser-wmpointer-l1-1-1.dll
 - MinUser.dll
 - API-Ms-Win-RTCore-NTUser-WMPointer-L1-1-2.dll
 - API-MS-Win-RTCore-NTUser-WMPointer-L1-1-3.dll
api_name:
 - RegisterPointerInputTarget
---

# RegisterPointerInputTarget function


## -description

Allows the caller to register a target window to which all pointer input of the specified type is redirected.

## -parameters

### -param hwnd [in]

The window to register as a global redirection target.

Redirection can cause the foreground window to lose activation (focus). To avoid this, ensure the window is a message-only window or has the <a href="/windows/desktop/winmsg/extended-window-styles">WS_EX_NOACTIVATE</a> style set.

### -param pointerType [in]

Type of pointer input to be redirected to the specified  window. This is any valid and supported value from the <a href="/windows/win32/api/winuser/ne-winuser-tagpointer_input_type">POINTER_INPUT_TYPE</a> enumeration. Note that the generic <b>PT_POINTER</b> type and the <b>PT_MOUSE</b> type are not valid in this parameter.

## -returns

If the function succeeds, the return value is non-zero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

An application with the UI Access privilege can use this function to register its own window to receive all input of the specified pointer input type. Each desktop allows only one such global redirection target window for each pointer input type at any given time. The first window to successfully register remains in effect until the window is unregistered or destroyed, at which point the role is available to the next qualified caller.

While the registration is in effect, all input of the specified pointer type, whether from an input device or injected by an application, is redirected to the registered window. However, when the process that owns the registered window injects input of the specified pointer type, such injected is not redirected but is instead processed normally.

An application that wishes to register the same window as a global redirection target for multiple pointer input types must call the <b>RegisterPointerInputTarget</b> function multiple times, once for each pointer input type of interest.

If the calling thread does not have the UI Access privilege, this function fails with the last error set to <b>ERROR_ACCESS_DENIED</b>.

If the specified pointer input type is not valid, this function fails with the last error set to <b>ERROR_INVALID_PARAMETER</b>.

If the calling thread does not own the specified window, this function fails with the last error set to <b>ERROR_ACCESS_DENIED</b>.

If the specified window’s desktop already has a registered global redirection target for the specified pointer input type, this function fails with the last error set to <b>ERROR_ACCESS_DENIED</b>.