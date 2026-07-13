---
UID: NF:winuser.GetPointerInputTransform
title: GetPointerInputTransform function (winuser.h)
description: Gets one or more transforms for the pointer information coordinates associated with the current message.
helpviewer_keywords: ["GetPointerInputTransform","GetPointerInputTransform function [Input Messages and Notifications]","inputmsg.getpointerinputtransform","winuser/GetPointerInputTransform"]
old-location: inputmsg\getpointerinputtransform.htm
tech.root: InputMsg
ms.assetid: 9F10ED61-90E3-441B-8F4D-E33DA54D473C
ms.date: 12/05/2018
ms.keywords: GetPointerInputTransform, GetPointerInputTransform function [Input Messages and Notifications], inputmsg.getpointerinputtransform, winuser/GetPointerInputTransform
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - GetPointerInputTransform
 - winuser/GetPointerInputTransform
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-wmpointermin-l1-1-0.dll
 - ext-ms-win-rtcore-ntuser-wmpointer-l1-1-0.dll
 - api-ms-win-rtcore-ntuser-wmpointer-l1-2-0.dll
 - User32.dll
 - API-MS-Win-RTCore-NTUser-WMPointer-l1-1-0.dll
 - MinUser.dll
 - API-MS-Win-RTCore-NTUser-WMPointer-l1-1-1.dll
 - API-Ms-Win-RTCore-NTUser-WMPointer-L1-1-2.dll
 - API-MS-Win-RTCore-NTUser-WMPointer-L1-1-3.dll
api_name:
 - GetPointerInputTransform
---

# GetPointerInputTransform function


## -description

Gets one or more transforms for the pointer information coordinates associated with the current message.

## -parameters

### -param pointerId [in]

An identifier of the pointer for which to retrieve information.

### -param historyCount [in]

The number of <a href="/windows/desktop/api/winuser/ns-winuser-input_transform">INPUT_TRANSFORM</a> structures that <i>inputTransform</i> can point to.

This value must be no less than 1 and no greater than the value specified in <b>historyCount</b> of the <a href="/windows/desktop/api/winuser/ns-winuser-pointer_info">POINTER_INFO</a> structure returned by <a href="/windows/desktop/api/winuser/nf-winuser-getpointerinfo">GetPointerInfo</a>, <a href="/windows/desktop/api/winuser/nf-winuser-getpointertouchinfo">GetPointerTouchInfo</a>, or <a href="/windows/desktop/api/winuser/nf-winuser-getpointerpeninfo">GetPointerPenInfo</a> (for a single input transform) or <a href="/windows/desktop/api/winuser/nf-winuser-getpointerinfohistory">GetPointerInfoHistory</a>, <a href="/windows/desktop/api/winuser/nf-winuser-getpointertouchinfohistory">GetPointerTouchInfoHistory</a>, or <a href="/windows/desktop/api/winuser/nf-winuser-getpointerpeninfohistory">GetPointerPenInfoHistory</a> (for an array of input transforms).

If <b>GetPointerInputTransform</b> succeeds, <i>inputTransform</i>  is updated with the total count of structures available. The total count of structures available is the same as the <b>historyCount</b> field of the <a href="/windows/desktop/api/winuser/ns-winuser-pointer_info">POINTER_INFO</a> structure.

### -param inputTransform [out]

Address of an array of <a href="/windows/desktop/api/winuser/ns-winuser-input_transform">INPUT_TRANSFORM</a> structures to receive the transform information. This parameter cannot be NULL.

## -returns

If the function succeeds, the return value is non-zero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

A consumer of pointer input messages typically uses <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient">ScreenToClient</a> or <a href="/windows/desktop/api/winuser/nf-winuser-mapwindowpoints">MapWindowPoints</a> to convert screen coordinates to client coordinates.

If a transform is applied on the message consumer, use <b>GetPointerInputTransform</b> to retrieve the transform on the message consumer at the time the input occurred. The inverse of this transform can then be used to convert pointer input coordinates from screen coordinates to the client coordinates of the message consumer.

If an input transform is not associated with the input, the <b>GetPointerInputTransform</b> function fails with the last error set to <b>ERROR_NO_DATA</b>. Use <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient">ScreenToClient</a> or <a href="/windows/desktop/api/winuser/nf-winuser-mapwindowpoints">MapWindowPoints</a> instead.

The input transform does not respect any right-to-left layout setting on the input target. An application that requires adjusted coordinates for right-to-left layout must perform the right-to-left mirroring  or combine an appropriate mirroring transform with the input transform.



The information returned by <b>GetPointerInputTransform</b> is associated with the most recent pointer message retrieved by the calling thread. When the next message is retrieved by the calling thread, the information associated with the previous message might no longer be available.

If an application calls <a href="/windows/desktop/api/winuser/nf-winuser-getpointerinfo">GetPointerInfo</a>, it can call <b>GetPointerInputTransform</b> with the same pointer Id and a single <a href="/windows/desktop/api/winuser/ns-winuser-input_transform">INPUT_TRANSFORM</a> output buffer to get the input transform associated with the data.

If an application calls <a href="/windows/desktop/api/winuser/nf-winuser-getpointerframeinfo">GetPointerFrameInfo</a>, it can call <b>GetPointerInputTransform</b> with the same pointer Id and a single <a href="/windows/desktop/api/winuser/ns-winuser-input_transform">INPUT_TRANSFORM</a> output buffer to get the input transform associated with the data. The same input transform applies to the entire frame.

If an application calls <a href="/windows/desktop/api/winuser/nf-winuser-getpointerinfohistory">GetPointerInfoHistory</a>, it can call <b>GetPointerInputTransform</b> with the same pointer Id and an output buffer to hold the entries retrieved using <b>GetPointerInfoHistory</b>. Each input transform in the returned array can be used with the corresponding entry in the array returned by <b>GetPointerInfoHistory</b>.

If an application calls <a href="/windows/desktop/api/winuser/nf-winuser-getpointerframeinfohistory">GetPointerFrameInfoHistory</a>, it can call <b>GetPointerInputTransform</b> with the same pointer Id and an output buffer to hold the entries retrieved using <a href="/windows/desktop/api/winuser/nf-winuser-getpointerinfohistory">GetPointerInfoHistory</a>. Each input transform in the returned array can be used with the corresponding frame in the array returned by <b>GetPointerFrameInfoHistory</b>, with the same input transform being applied to the entire frame.



If the information associated with the message is no longer available, this function fails with the last error set to <b>ERROR_INVALID_PARAMETER</b>.

If <i>historyCount</i> contains a value larger than the <b>historyCount</b> field of the <a href="/windows/desktop/api/winuser/ns-winuser-pointer_info">POINTER_INFO</a> structure returned by <a href="/windows/desktop/api/winuser/nf-winuser-getpointerinfo">GetPointerInfo</a> (or the first <b>POINTER_INFO</b> structure in the array returned by <a href="/windows/desktop/api/winuser/nf-winuser-getpointerinfohistory">GetPointerInfoHistory</a>), the function fails with the last error set to <b>ERROR_INVALID_PARAMETER</b>.

## -see-also

<a href="/windows/win32/inputmsg/functions">Functions</a>



<a href="/windows/desktop/api/winuser/ns-winuser-input_transform">INPUT_TRANSFORM</a>