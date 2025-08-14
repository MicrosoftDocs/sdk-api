---
UID: NF:winuser.GetPointerPenInfo
title: GetPointerPenInfo function (winuser.h)
description: Gets the pen-based information for the specified pointer (of type PT_PEN) associated with the current message.
helpviewer_keywords: ["GetPointerPenInfo","GetPointerPenInfo function [Input Messages and Notifications]","inputmsg.getpointerpeninfo","winuser/GetPointerPenInfo"]
old-location: inputmsg\getpointerpeninfo.htm
tech.root: InputMsg
ms.assetid: 5f1f7252-a4aa-4b06-94c9-2aa365cf0100
ms.date: 12/05/2018
ms.keywords: GetPointerPenInfo, GetPointerPenInfo function [Input Messages and Notifications], inputmsg.getpointerpeninfo, winuser/GetPointerPenInfo
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
 - GetPointerPenInfo
 - winuser/GetPointerPenInfo
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
 - API-MS-Win-RTCore-NTUser-WMPointer-l1-1-0.dll
 - MinUser.dll
 - API-MS-Win-RTCore-NTUser-WMPointer-l1-1-1.dll
 - API-Ms-Win-RTCore-NTUser-WMPointer-L1-1-2.dll
 - API-MS-Win-RTCore-NTUser-WMPointer-L1-1-3.dll
api_name:
 - GetPointerPenInfo
---

# GetPointerPenInfo function


## -description

Gets the pen-based information for the specified pointer (of type <a href="/windows/win32/api/winuser/ne-winuser-tagpointer_input_type">PT_PEN</a>) associated with the current message.

## -parameters

### -param pointerId [in]

An identifier of the pointer for which to retrieve information.

### -param penInfo [out]

Address of a <a href="/windows/desktop/api/winuser/ns-winuser-pointer_pen_info">POINTER_PEN_INFO</a> structure to receive the pen-specific pointer information.

## -returns

If the function succeeds, the return value is non-zero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>GetPointerPenInfo</b> retrieves information for a single pointer (of type <a href="/windows/win32/api/winuser/ne-winuser-tagpointer_input_type">PT_PEN</a>) associated with a pointer message. 

Use <a href="/windows/desktop/api/winuser/nf-winuser-getpointerframepeninfo">GetPointerFramePenInfo</a> to retrieve frame information associated with a message  for a set of pointers.

The information returned by <a href="/windows/desktop/api/winuser/nf-winuser-getpointerinfo">GetPointerInfo</a> is associated with the most recent pointer message retrieved by the calling thread. When the next message is retrieved by the calling thread, the information associated with the previous message may no longer be available.

If the application does not process pointer input messages as fast as they are generated, some messages may be coalesced into a <a href="/windows/win32/inputmsg/wm-pointerupdate">WM_POINTERUPDATE</a> message. Use <a href="/windows/desktop/api/winuser/nf-winuser-getpointerpeninfohistory">GetPointerPenInfoHistory</a> to retrieve the message history from the most recent <b>WM_POINTERUPDATE</b> message. 

If the information associated with the message is no longer available, this function fails with the last error set to <b>ERROR_NO_DATA</b>.

If the calling thread does not own the window to which the pointer message has been delivered, this function fails with the last error set to <b>ERROR_ACCESS_DENIED</b>. Note that this may be the window to which the input was originally delivered or it may be a window to which the message was forwarded.

If the specified pointer is not of type <a href="/windows/win32/api/winuser/ne-winuser-tagpointer_input_type">PT_PEN</a>, this function fails with the last error set to <b>ERROR_DATATYPE_MISMATCH</b>.

## -see-also

<a href="/windows/win32/inputmsg/functions">Functions</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getpointerframepeninfo">GetPointerFramePenInfo</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getpointerframepeninfohistory">GetPointerFramePenInfoHistory</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getpointerpeninfohistory">GetPointerPenInfoHistory</a>