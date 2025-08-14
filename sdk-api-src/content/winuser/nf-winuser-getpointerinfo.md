---
UID: NF:winuser.GetPointerInfo
title: GetPointerInfo function (winuser.h)
description: Gets the information for the specified pointer associated with the current message.
helpviewer_keywords: ["GetPointerInfo","GetPointerInfo function [Input Messages and Notifications]","inputmsg.getpointerinfo","winuser/GetPointerInfo"]
old-location: inputmsg\getpointerinfo.htm
tech.root: InputMsg
ms.assetid: 75faea24-91cd-448b-b67a-19fe530f1800
ms.date: 12/05/2018
ms.keywords: GetPointerInfo, GetPointerInfo function [Input Messages and Notifications], inputmsg.getpointerinfo, winuser/GetPointerInfo
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
 - GetPointerInfo
 - winuser/GetPointerInfo
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
 - GetPointerInfo
req.apiset: ext-ms-win-rtcore-ntuser-wmpointer-l1-1-0 (introduced in Windows 10, version 10.0.14393)
---

# GetPointerInfo function


## -description

Gets the information for the specified pointer associated with the current message.
<div class="alert"><b>Note</b>  Use <a href="/windows/desktop/api/winuser/nf-winuser-getpointertype">GetPointerType</a> if you don't need the additional information exposed by <b>GetPointerInfo</b>.</div><div> </div>

## -parameters

### -param pointerId [in]

The pointer identifier.

### -param pointerInfo [out]

Address of a  <a href="/windows/desktop/api/winuser/ns-winuser-pointer_info">POINTER_INFO</a> structure that receives the pointer information.

## -returns

If the function succeeds, the return value is non-zero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>GetPointerInfo</b> retrieves information for a single pointer associated with a pointer message. 

Use <a href="/windows/desktop/api/winuser/nf-winuser-getpointerframeinfo">GetPointerFrameInfo</a> to retrieve frame information associated with a message  for a set of pointers.

The information returned by <b>GetPointerInfo</b> is associated with the most recent pointer message retrieved by the calling thread. When the next message is retrieved by the calling thread, the information associated with the previous message may no longer be available.

If the application does not process pointer input messages as fast as they are generated, some messages may be coalesced into a <a href="/windows/win32/inputmsg/wm-pointerupdate">WM_POINTERUPDATE</a> message. Use <a href="/windows/desktop/api/winuser/nf-winuser-getpointerinfohistory">GetPointerInfoHistory</a> to retrieve the message history from the most recent <b>WM_POINTERUPDATE</b> message. 

If the information associated with the message is no longer available, this function fails with the last error set to <b>ERROR_NO_DATA</b>.

If the calling thread does not own the window to which the pointer message has been delivered, this function fails with the last error set to <b>ERROR_ACCESS_DENIED</b>. Note that this may be the window to which the input was originally delivered or it may be a window to which the message was forwarded.

## -see-also

<a href="/windows/win32/inputmsg/functions">Functions</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getpointerframeinfo">GetPointerFrameInfo</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getpointerframeinfohistory">GetPointerFrameInfoHistory</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getpointerinfohistory">GetPointerInfoHistory</a>
