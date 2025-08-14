---
UID: NF:winuser.GetPointerTouchInfo
title: GetPointerTouchInfo function (winuser.h)
description: Gets the touch-based information for the specified pointer (of type PT_TOUCH) associated with the current message.
helpviewer_keywords: ["GetPointerTouchInfo","GetPointerTouchInfo function [Input Messages and Notifications]","inputmsg.getpointertouchinfo","winuser/GetPointerTouchInfo"]
old-location: inputmsg\getpointertouchinfo.htm
tech.root: InputMsg
ms.assetid: 97d93754-fc7e-4400-a6ee-6bab53e421cf
ms.date: 12/05/2018
ms.keywords: GetPointerTouchInfo, GetPointerTouchInfo function [Input Messages and Notifications], inputmsg.getpointertouchinfo, winuser/GetPointerTouchInfo
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
 - GetPointerTouchInfo
 - winuser/GetPointerTouchInfo
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
 - API-MS-Win-NTUser-IE-WMPointer-l1-1-0.dll
 - ie_shims.dll
 - API-MS-Win-RTCore-NTUser-WMPointer-l1-1-0.dll
 - MinUser.dll
 - API-MS-Win-RTCore-NTUser-WMPointer-l1-1-1.dll
 - API-Ms-Win-RTCore-NTUser-WMPointer-L1-1-2.dll
 - API-MS-Win-RTCore-NTUser-WMPointer-L1-1-3.dll
api_name:
 - GetPointerTouchInfo
---

# GetPointerTouchInfo function


## -description

Gets the touch-based information for the specified pointer (of type <a href="/windows/win32/api/winuser/ne-winuser-tagpointer_input_type">PT_TOUCH</a>) associated with the current message.

## -parameters

### -param pointerId [in]

An identifier of the pointer for which to retrieve information.

### -param touchInfo [out]

Address of a <a href="/windows/desktop/api/winuser/ns-winuser-pointer_touch_info">POINTER_TOUCH_INFO</a> structure to receive the touch-specific pointer information.

## -returns

If the function succeeds, the return value is non-zero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>GetPointerTouchInfo</b> retrieves information for a single pointer (of type <a href="/windows/win32/api/winuser/ne-winuser-tagpointer_input_type">PT_TOUCH</a>) associated with a pointer message. 

Use <a href="/windows/desktop/api/winuser/nf-winuser-getpointerframetouchinfo">GetPointerFrameTouchInfo</a> to retrieve frame information associated with a message  for a set of pointers.

The information returned by <b>GetPointerTouchInfo</b> is associated with the most recent pointer message retrieved by the calling thread. When the next message is retrieved by the calling thread, the information associated with the previous message may no longer be available.

If the application does not process pointer input messages as fast as they are generated, some messages may be coalesced into a <a href="/windows/win32/inputmsg/wm-pointerupdate">WM_POINTERUPDATE</a> message. Use <a href="/windows/desktop/api/winuser/nf-winuser-getpointertouchinfohistory">GetPointerTouchInfoHistory</a> to retrieve the message history from the most recent <b>WM_POINTERUPDATE</b> message. 

If the information associated with the message is no longer available, this function fails with the last error set to <b>ERROR_NO_DATA</b>.

If the calling thread does not own the window to which the pointer message has been delivered, this function fails with the last error set to <b>ERROR_ACCESS_DENIED</b>. Note that this may be the window to which the input was originally delivered or it may be a window to which the message was forwarded.

If the specified pointer is not of type <a href="/windows/win32/api/winuser/ne-winuser-tagpointer_input_type">PT_TOUCH</a>, this function fails with the last error set to <b>ERROR_DATATYPE_MISMATCH</b>.

## -see-also

<a href="/windows/win32/inputmsg/functions">Functions</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getpointerframetouchinfo">GetPointerFrameTouchInfo</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getpointerframetouchinfohistory">GetPointerFrameTouchInfoHistory</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getpointertouchinfohistory">GetPointerTouchInfoHistory</a>