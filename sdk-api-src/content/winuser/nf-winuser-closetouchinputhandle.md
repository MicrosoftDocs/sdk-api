---
UID: NF:winuser.CloseTouchInputHandle
title: CloseTouchInputHandle function (winuser.h)
description: Closes a touch input handle, frees process memory associated with it, and invalidates the handle.
helpviewer_keywords: ["CloseTouchInputHandle","CloseTouchInputHandle function [Windows Touch]","wintouch.closetouchinputhandle","winuser/CloseTouchInputHandle"]
old-location: wintouch\closetouchinputhandle.htm
tech.root: wintouch
ms.assetid: bdc8bb94-3126-4183-9dfd-ba4844d98f29
ms.date: 12/05/2018
ms.keywords: CloseTouchInputHandle, CloseTouchInputHandle function [Windows Touch], wintouch.closetouchinputhandle, winuser/CloseTouchInputHandle
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
 - CloseTouchInputHandle
 - winuser/CloseTouchInputHandle
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
 - ext-ms-win-ntuser-misc-l1-3-0.dll
 - ext-ms-win-ntuser-misc-l1-2-0.dll
 - user32.dll
api_name:
 - CloseTouchInputHandle
---

# CloseTouchInputHandle function


## -description

Closes a touch input handle, frees process memory associated with it, and invalidates the handle.

## -parameters

### -param hTouchInput [in]

The touch input handle received in the <b>LPARAM</b> of a touch message. The function fails with <b>ERROR_INVALID_HANDLE</b> if this handle is not valid. Note that the handle is not valid after it has been used in a successful call to <b>CloseTouchInputHandle</b> or after it has been passed to <a href="/windows/desktop/wintouch/sendmessage--postmessage--and-related-functions">DefWindowProc, PostMessage, SendMessage</a> or one of their variants.

## -returns

If the function succeeds, the return value is nonzero.
     



If the function fails, the return value is zero. To get extended error information, use the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -remarks

Calling <b>CloseTouchInputHandle</b> will not free memory associated with values retrieved in a call to <a href="/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo">GetTouchInputInfo</a>. Values in structures passed to <b>GetTouchInputInfo</b>  will be valid until you delete them.

## -see-also

<a href="/windows/desktop/wintouch/mtfunctions">Functions</a>



<a href="/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo">GetTouchInputInfo</a>