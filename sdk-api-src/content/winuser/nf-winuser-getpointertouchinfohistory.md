---
UID: NF:winuser.GetPointerTouchInfoHistory
title: GetPointerTouchInfoHistory function (winuser.h)
description: Gets the touch-based information associated with the individual inputs, if any, that were coalesced into the current message for the specified pointer (of type PT_TOUCH).
helpviewer_keywords: ["GetPointerTouchInfoHistory","GetPointerTouchInfoHistory function [Input Messages and Notifications]","inputmsg.getpointertouchinfohistory","winuser/GetPointerTouchInfoHistory"]
old-location: inputmsg\getpointertouchinfohistory.htm
tech.root: InputMsg
ms.assetid: 9fdfbde7-4126-4c1b-b870-479f846e1aa9
ms.date: 12/05/2018
ms.keywords: GetPointerTouchInfoHistory, GetPointerTouchInfoHistory function [Input Messages and Notifications], inputmsg.getpointertouchinfohistory, winuser/GetPointerTouchInfoHistory
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
 - GetPointerTouchInfoHistory
 - winuser/GetPointerTouchInfoHistory
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
 - GetPointerTouchInfoHistory
---

# GetPointerTouchInfoHistory function


## -description

Gets the touch-based information associated with the individual inputs, if any, that were coalesced into the current message for the specified pointer (of type <a href="/windows/win32/api/winuser/ne-winuser-tagpointer_input_type">PT_TOUCH</a>). The most recent input is included in the returned history and is the same as the most recent input returned by the <a href="/windows/desktop/api/winuser/nf-winuser-getpointertouchinfo">GetPointerTouchInfo</a> function.

## -parameters

### -param pointerId [in]

An identifier of the pointer for which to retrieve information.

### -param entriesCount [in, out]

A pointer to a variable that specifies the count of structures in the buffer to which touchInfo points. If <b>GetPointerTouchInfoHistory</b> succeeds, <i>entriesCount</i> is updated with the total count of structures available. The total count of structures available is the same as the <i>historyCount</i> field in the <a href="/windows/desktop/api/winuser/ns-winuser-pointer_info">POINTER_INFO</a> structure returned by a call to <a href="/windows/desktop/api/winuser/nf-winuser-getpointerinfo">GetPointerInfo</a> or <a href="/windows/desktop/api/winuser/nf-winuser-getpointertouchinfo">GetPointerTouchInfo</a>.

### -param touchInfo [out, optional]

Address of an array of <a href="/windows/desktop/api/winuser/ns-winuser-pointer_touch_info">POINTER_TOUCH_INFO</a> structures to receive the pointer information. This parameter can be NULL if *entriesCount is zero.

## -returns

If the function succeeds, the return value is non-zero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If the application does not process pointer input messages as fast as they are generated, some moves may be coalesced. When an application receives a coalescable pointer (of type <a href="/windows/win32/api/winuser/ne-winuser-tagpointer_input_type">PT_TOUCH</a>) message, it can use the <b>GetPointerTouchInfoHistory</b> function to retrieve information for all the individual inputs, if any, that were coalesced into the message. Note that the information retrieved is associated with the pointer message most recently retrieved by the calling thread. Once the calling thread retrieves its next message, the information associated with the previous message may no longer be available.

The information retrieved appears in reverse chronological order, with the most recent entry in the first row of the returned array. The most recent entry is the same as that returned by the <a href="/windows/desktop/api/winuser/nf-winuser-getpointertouchinfo">GetPointerTouchInfo</a> function.

If the count of rows in the buffer provided is insufficient to hold all available history entries, this function succeeds with the buffer containing the most recent entries and <i>*entriesCount</i> containing the total count of entries available.


If the pointer frame contains no additional pointers besides the specified pointer, this function succeeds and returns only the information for the specified pointer.

If the information associated with the pointer frame is no longer available, this function fails with the last error set to <b>ERROR_NO_DATA</b>.

If the calling thread does not own the window (where the input was originally delivered or where the message was forwarded) to which the pointer message has been delivered, this function fails with the last error set to <b>ERROR_ACCESS_DENIED</b>. 

If the specified pointer is not of type <a href="/windows/win32/api/winuser/ne-winuser-tagpointer_input_type">PT_TOUCH</a>, this function fails with the last error set to <b>ERROR_DATATYPE_MISMATCH</b>.

## -see-also

<a href="/windows/win32/inputmsg/functions">Functions</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getpointerframetouchinfo">GetPointerFrameTouchInfo</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getpointerframetouchinfohistory">GetPointerFrameTouchInfoHistory</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getpointertouchinfo">GetPointerTouchInfo</a>