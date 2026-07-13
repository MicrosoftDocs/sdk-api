---
UID: NF:winuser.IsMouseInPointerEnabled
title: IsMouseInPointerEnabled function (winuser.h)
description: Indicates whether EnableMouseInPointer is set for the mouse to act as a pointer input device and send WM_POINTER messages.
helpviewer_keywords: ["IsMouseInPointerEnabled","IsMouseInPointerEnabled function [Keyboard and Mouse Input]","inputdev.ismouseinpointerenabled","inputmsg.ismouseinpointerenabled","winuser/IsMouseInPointerEnabled"]
old-location: inputmsg\ismouseinpointerenabled.htm
tech.root: InputMsg
ms.assetid: 5D493066-2425-4610-8489-575BF25C8C16
ms.date: 12/05/2018
ms.keywords: IsMouseInPointerEnabled, IsMouseInPointerEnabled function [Keyboard and Mouse Input], inputdev.ismouseinpointerenabled, inputmsg.ismouseinpointerenabled, winuser/IsMouseInPointerEnabled
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
 - IsMouseInPointerEnabled
 - winuser/IsMouseInPointerEnabled
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
 - API-MS-Win-RTCore-NTUser-WMPointer-L1-1-0.dll
 - API-MS-Win-RTCore-NTUser-WMPointer-L1-1-1.dll
 - MinUser.dll
 - API-Ms-Win-RTCore-NTUser-WMPointer-L1-1-2.dll
 - API-MS-Win-RTCore-NTUser-WMPointer-L1-1-3.dll
api_name:
 - IsMouseInPointerEnabled
---

# IsMouseInPointerEnabled function


## -description

Indicates whether <a href="/windows/desktop/api/winuser/nf-winuser-enablemouseinpointer">EnableMouseInPointer</a> is set for the mouse to  act as a pointer input device and send <a href="/windows/win32/inputmsg/messages">WM_POINTER</a> messages.



## -returns

If <a href="/windows/desktop/api/winuser/nf-winuser-enablemouseinpointer">EnableMouseInPointer</a> is set, the return value is nonzero.

If <a href="/windows/desktop/api/winuser/nf-winuser-enablemouseinpointer">EnableMouseInPointer</a> is not set, the return value is zero.

## -remarks

<a href="/windows/desktop/api/winuser/nf-winuser-enablemouseinpointer">EnableMouseInPointer</a> can be called only once in the context of a process lifetime.  Prior to the first call, Windows Store apps run with mouse-in-pointer enabled, as do any desktop applications that consume mshtml.dll.  All other desktop applications run with mouse-in-pointer disabled.

On the first call to <a href="/windows/desktop/api/winuser/nf-winuser-enablemouseinpointer">EnableMouseInPointer</a> in the process lifetime, the state is changed as specified and the call succeeds.

On subsequent calls to <a href="/windows/desktop/api/winuser/nf-winuser-enablemouseinpointer">EnableMouseInPointer</a>, the state will not change.  If the current state is not equal to the specified state, the call fails.

Call <b>IsMouseInPointerEnabled</b> to verify the mouse-in-pointer state.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-enablemouseinpointer">EnableMouseInPointer</a>



<a href="/windows/win32/inputmsg/functions">Functions</a>



<a href="/windows/win32/inputmsg/messages">WM_POINTER</a>
