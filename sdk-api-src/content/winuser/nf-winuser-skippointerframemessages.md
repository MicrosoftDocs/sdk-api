---
UID: NF:winuser.SkipPointerFrameMessages
title: SkipPointerFrameMessages function (winuser.h)
description: Determines which pointer input frame generated the most recently retrieved message for the specified pointer and discards any queued (unretrieved) pointer input messages generated from the same pointer input frame.
helpviewer_keywords: ["SkipPointerFrameMessages","SkipPointerFrameMessages function [Input Messages and Notifications]","inputmsg.skippointerframemessages","winuser/SkipPointerFrameMessages"]
old-location: inputmsg\skippointerframemessages.htm
tech.root: InputMsg
ms.assetid: d67f8d44-3e19-4523-a0f3-38f09f5df91f
ms.date: 12/05/2018
ms.keywords: SkipPointerFrameMessages, SkipPointerFrameMessages function [Input Messages and Notifications], inputmsg.skippointerframemessages, winuser/SkipPointerFrameMessages
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
 - SkipPointerFrameMessages
 - winuser/SkipPointerFrameMessages
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
 - api-ms-win-rtcore-ntuser-wmpointer-l1-1-0.dll
 - API-Ms-Win-RTCore-NTUser-WMPointer-L1-1-2.dll
 - API-MS-Win-RTCore-NTUser-WMPointer-L1-1-3.dll
api_name:
 - SkipPointerFrameMessages
---

# SkipPointerFrameMessages function


## -description

Determines which pointer input frame generated the most recently retrieved message for the specified pointer and discards any queued (unretrieved) pointer input messages generated from the same pointer input frame. If an application has retrieved information for an entire frame using the <a href="/windows/desktop/api/winuser/nf-winuser-getpointerframeinfo">GetPointerFrameInfo</a> function, the <a href="/windows/desktop/api/winuser/nf-winuser-getpointerframeinfohistory">GetPointerFrameInfoHistory</a> function or one of their type-specific variants, it can use this function to avoid retrieving and discarding remaining messages from that frame one by one.

## -parameters

### -param pointerId [in]

Identifier of the pointer. Pending messages will be skipped for the frame that includes the most recently retrieved input for this pointer.

## -returns

If the function succeeds, the return value is non-zero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Parallel-mode devices may report pointer input in frames, that is, they may report the state and position of all pointers from that device in a single input report to the system. Ideally, applications should view the entire frame as a single input unless the application-specific requirements dictate otherwise.

The <b>SkipPointerFrameMessages</b> function can be used in conjunction with the <a href="/windows/desktop/api/winuser/nf-winuser-getpointerframeinfo">GetPointerFrameInfo</a> function (or one of its type-specific variants) to consume entire frames as a single input.

When an application sees a pointer message, it can use the <a href="/windows/desktop/api/winuser/nf-winuser-getpointerframeinfo">GetPointerFrameInfo</a> function to retrieve the entire pointer input frame to which the pointer message belongs, hence obtaining an updated view of all of the pointers currently owned by the window. Note that the returned frame contains only pointers that are currently owned by the same window as the specified pointer.

Having retrieved the entire frame of information, the application can then call the <b>SkipPointerFrameMessages</b> function to skip remaining pointer messages associated with this frame that are pending retrieval. This saves the application the overhead of retrieving and processing the remaining messages one by one.

<div class="alert"><b>Warning</b>  The <b>SkipPointerFrameMessages</b> function should be used only when the caller can be sure that no other entity on the caller’s thread (such as  <a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a>) is expecting to retrieve pending pointer messages. For this reason, <b>SkipPointerFrameMessages</b> should not be used in conjunction with Direct Manipulation when processing multiple, simultaneous interactions.</div>
<div> </div>
Note that the information retrieved is associated with the pointer frame most recently retrieved by the calling thread. Once the calling thread retrieves its next message, the information associated with the previous pointer frame may no longer be available.

If the pointer frame contains no additional pointers besides the specified pointer, this function succeeds with no action.

If the calling thread does not own the window to which the pointer message has been delivered, this function fails with the last error set to <b>ERROR_ACCESS_DENIED</b>.

## -see-also

<a href="/windows/win32/inputmsg/functions">Functions</a>