---
UID: NF:winuser.UnregisterPointerInputTarget
title: UnregisterPointerInputTarget function (winuser.h)
description: Allows the caller to unregister a target window to which all pointer input of the specified type is redirected.
helpviewer_keywords: ["UnregisterPointerInputTarget","UnregisterPointerInputTarget function [Windows Accessibility]","inputmsg.getactivepointers","winauto.unregisterpointerinputtarget","winuser/UnregisterPointerInputTarget"]
old-location: winauto\unregisterpointerinputtarget.htm
tech.root: WinAuto
ms.assetid: 75faea24-91cd-448b-b67a-09fe530f1800
ms.date: 12/05/2018
ms.keywords: UnregisterPointerInputTarget, UnregisterPointerInputTarget function [Windows Accessibility], inputmsg.getactivepointers, winauto.unregisterpointerinputtarget, winuser/UnregisterPointerInputTarget
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
 - UnregisterPointerInputTarget
 - winuser/UnregisterPointerInputTarget
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
 - API-MS-Win-RTCore-NTUser-WMPointer-l1-1-1.dll
 - MinUser.dll
 - API-Ms-Win-RTCore-NTUser-WMPointer-L1-1-2.dll
 - API-MS-Win-RTCore-NTUser-WMPointer-L1-1-3.dll
api_name:
 - UnregisterPointerInputTarget
---

# UnregisterPointerInputTarget function


## -description

Allows the caller to unregister a target window to which all pointer input of the specified type is redirected.

## -parameters

### -param hwnd [in]

Window to be un-registered as a global redirection target on its desktop.

### -param pointerType [in]

Type of pointer input to no longer be redirected to the specified window. This is any valid and supported value from the <a href="/windows/win32/api/winuser/ne-winuser-tagpointer_input_type">POINTER_INPUT_TYPE </a> enumeration. Note that the generic <b>PT_POINTER</b> type and the<b> PT_MOUSE</b> type are not valid in this parameter.

## -returns

If the function succeeds, the return value is non-zero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

An application that has successfully called the <a href="/windows/desktop/api/winuser/nf-winuser-registerpointerinputtarget">RegisterPointerInputTarget</a> function can call this function to un-register the window from the role of global redirected target for the specified pointer type.

An application that has registered the same window as a global redirection target for multiple pointer input types can call the <b>UnregisterPointerInputTarget</b> to un-register the window for one of those types while leaving the window registered for the remaining types.

If the calling thread does not have the UI Access privilege, this function fails with the last error set to <b>ERROR_ACCESS_DENIED</b>.

If the specified pointer input type is not valid, this function fails with the last error set to <b>ERROR_INVALID_PARAMETER</b>.

If the calling thread does not own the specified window, this function fails with the last error set to <b>ERROR_ACCESS_DENIED</b>.

If the specified window is not the registered global redirection target for the specified pointer input type on its desktop, this function takes no action and returns success.