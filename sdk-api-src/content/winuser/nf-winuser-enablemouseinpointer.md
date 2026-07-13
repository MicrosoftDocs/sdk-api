---
UID: NF:winuser.EnableMouseInPointer
title: EnableMouseInPointer function (winuser.h)
description: Enables the mouse to act as a pointer input device and send WM_POINTER messages.
helpviewer_keywords: ["EnableMouseInPointer","EnableMouseInPointer function [Keyboard and Mouse Input]","inputdev.enablemouseinpointer","inputmsg.enablemouseinpointer","winuser/EnableMouseInPointer"]
old-location: inputmsg\enablemouseinpointer.htm
tech.root: InputMsg
ms.assetid: 66D9BF17-164F-455F-803F-36CDF88C34FF
ms.date: 12/05/2018
ms.keywords: EnableMouseInPointer, EnableMouseInPointer function [Keyboard and Mouse Input], inputdev.enablemouseinpointer, inputmsg.enablemouseinpointer, winuser/EnableMouseInPointer
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
 - EnableMouseInPointer
 - winuser/EnableMouseInPointer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-wmpointermin-l1-1-0.dll
 - ext-ms-win-ntuser-misc-l1-7-0.dll
 - ext-ms-win-ntuser-misc-l1-6-0.dll
 - ext-ms-win-ntuser-misc-l1-5-1.dll
 - ext-ms-win-ntuser-misc-l1-5-0.dll
 - ext-ms-win-ntuser-misc-l1-3-0.dll
 - ext-ms-win-ntuser-misc-l1-2-0.dll
 - ext-ms-win-ntuser-misc-l1-1-0.dll
 - api-ms-win-rtcore-ntuser-wmpointer-l1-2-0.dll
 - User32.dll
 - MinUser.dll
 - API-MS-Win-RTCore-NTUser-WMPointer-l1-1-0.dll
 - API-MS-Win-RTCore-NTUser-WMPointer-l1-1-1.dll
 - API-Ms-Win-RTCore-NTUser-WMPointer-L1-1-2.dll
 - API-MS-Win-RTCore-NTUser-WMPointer-L1-1-3.dll
api_name:
 - EnableMouseInPointer
---

# EnableMouseInPointer function


## -description

Enables the mouse to act as a pointer input device and send <a href="/windows/win32/inputmsg/messages">WM_POINTER</a> messages.

## -parameters

### -param fEnable [in]

<b>TRUE</b> to turn on mouse input support in <a href="/windows/win32/inputmsg/messages">WM_POINTER</a>.

## -returns

If the function succeeds, the return value is non-zero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function can be called only once in the context of a process lifetime.  Prior to the first call, Windows Store apps run with mouse-in-pointer enabled, as do any desktop applications that consume mshtml.dll.  All other desktop applications run with mouse-in-pointer disabled.

On the first call in the process lifetime, the state is changed as specified and the call succeeds.

On subsequent calls, the state will not change.  If the current state is not equal to the specified state, the call fails.

Call <a href="/windows/desktop/api/winuser/nf-winuser-ismouseinpointerenabled">IsMouseInPointerEnabled</a> to verify the mouse-in-pointer state.

## -see-also

<a href="/windows/win32/inputmsg/functions">Functions</a>



<a href="/windows/desktop/api/winuser/nf-winuser-ismouseinpointerenabled">IsMouseInPointerEnabled</a>



<a href="/windows/win32/inputmsg/messages">WM_POINTER</a>