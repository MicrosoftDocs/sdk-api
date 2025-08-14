---
UID: NF:winuser.GetPointerFramePenInfo
title: GetPointerFramePenInfo function (winuser.h)
description: Gets the entire frame of pen-based information for the specified pointers (of type PT_PEN) associated with the current message.
helpviewer_keywords: ["GetPointerFramePenInfo","GetPointerFramePenInfo function [Input Messages and Notifications]","inputmsg.getpointerframepeninfo","winuser/GetPointerFramePenInfo"]
old-location: inputmsg\getpointerframepeninfo.htm
tech.root: InputMsg
ms.assetid: 52db9b96-7f9e-41d7-88f7-b9c7691a6511
ms.date: 12/05/2018
ms.keywords: GetPointerFramePenInfo, GetPointerFramePenInfo function [Input Messages and Notifications], inputmsg.getpointerframepeninfo, winuser/GetPointerFramePenInfo
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
 - GetPointerFramePenInfo
 - winuser/GetPointerFramePenInfo
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
 - GetPointerFramePenInfo
---

# GetPointerFramePenInfo function


## -description

Gets the entire frame of pen-based information for the specified pointers (of type <a href="/windows/win32/api/winuser/ne-winuser-tagpointer_input_type">PT_PEN</a>) associated with the current message.

## -parameters

### -param pointerId [in]

An identifier of the pointer for which to retrieve frame information.

### -param pointerCount [in, out]

A pointer to a variable that specifies the count of structures in the buffer to which penInfo points. If <b>GetPointerFramePenInfo</b> succeeds, <i>pointerCount</i>  is updated with the total count of pointers in the frame.

### -param penInfo [out]

Address of an array of <a href="/windows/desktop/api/winuser/ns-winuser-pointer_pen_info">POINTER_PEN_INFO</a> structures to receive the pointer information. This parameter can be NULL if <i>*pointerCount</i> is zero.

## -returns

If the function succeeds, the return value is non-zero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Parallel-mode devices may report pointer input in frames, that is, they may report the state and position of all pointers from that device in a single input report to the system. Ideally, applications should view the entire frame as a single input unless the application-specific requirements dictate otherwise.

<b>GetPointerFramePenInfo</b> retrieves the entire pointer input frame associated with a pointer (of type <a href="/windows/win32/api/winuser/ne-winuser-tagpointer_input_type">PT_PEN</a>) message. Use <a href="/windows/desktop/api/winuser/nf-winuser-getpointerpeninfo">GetPointerPenInfo</a> to retrieve information for a single pointer associated with a pointer message.

The  frame contains only pointers that are currently owned by the same window as the specified pointer.

The information returned by <a href="/windows/desktop/api/winuser/nf-winuser-getpointerframeinfo">GetPointerFrameInfo</a> is associated with the most recent pointer message retrieved by the calling thread. When the next message is retrieved by the calling thread, the information associated with the previous message may no longer be available.



If the application does not process pointer input messages as fast as they are generated, some messages may be coalesced into a <a href="/windows/win32/inputmsg/wm-pointerupdate">WM_POINTERUPDATE</a> message. Use <a href="/windows/desktop/api/winuser/nf-winuser-getpointerframepeninfohistory">GetPointerFramePenInfoHistory</a> to retrieve the message history from the most recent <b>WM_POINTERUPDATE</b> message. 

Having retrieved the entire frame of information, the application can then call the <a href="/windows/desktop/api/winuser/nf-winuser-skippointerframemessages">SkipPointerFrameMessages</a> function to skip remaining pointer messages associated with this frame that are pending retrieval. This saves the application the overhead of retrieving and processing the remaining messages one by one. However, the <b>SkipPointerFrameMessages</b> function should be used with care and only when the caller can be sure that no other entity on the caller’s thread is expecting to see the remaining pointer messages one by one as they are retrieved.

Note that the information retrieved is associated with the pointer frame most recently retrieved by the calling thread. Once the calling thread retrieves its next message, the information associated with the previous pointer frame may no longer be available.

If the pointer frame contains no additional pointers besides the specified pointer, this function succeeds and returns only the information for the specified pointer.

If the information associated with the pointer frame is no longer available, this function fails with the last error set to <b>ERROR_NO_DATA</b>.

If the calling thread does not own the window to which the pointer message has been delivered, this function fails with the last error set to <b>ERROR_ACCESS_DENIED</b>.

If the specified pointer is not of type <a href="/windows/win32/api/winuser/ne-winuser-tagpointer_input_type">PT_PEN</a>, this function fails with the last error set to <b>ERROR_DATATYPE_MISMATCH</b>.



For apps that have  both client and non-client areas, the input frame can include both client and non-client data. To differentiate between client and non-client data, you must perform hit testing on the target window.

We recommend the following if you want to filter data from the input frame:

<ul>
<li>For each update that does not include a pointer contact (a <a href="/windows/win32/inputmsg/pointer-flags-contants">POINTER_FLAG_UPDATE</a> without <b>POINTER_FLAG_INCONTACT</b>), hit test to determine if the input is client or non-client.</li>
<li>For each new contact (<a href="/windows/win32/inputmsg/pointer-flags-contants">POINTER_FLAG_DOWN</a>), hit test to determine if the input is client or non-client and track this info.</li>
<li>For each update that includes a pointer contact (a <a href="/windows/win32/inputmsg/pointer-flags-contants">POINTER_FLAG_UPDATE</a> with <b>POINTER_FLAG_INCONTACT</b>), use the tracking info to determine whether the input is client or non-client.</li>
<li>For each <a href="/windows/win32/inputmsg/pointer-flags-contants">POINTER_FLAG_UP</a>, use the tracking info to determine whether the input is client or non-client and then clear this pointer from the tracking data.</li>
</ul>

## -see-also

<a href="/windows/win32/inputmsg/functions">Functions</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getpointerframepeninfohistory">GetPointerFramePenInfoHistory</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getpointerpeninfo">GetPointerPenInfo</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getpointerpeninfohistory">GetPointerPenInfoHistory</a>