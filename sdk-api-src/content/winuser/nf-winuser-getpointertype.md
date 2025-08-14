---
UID: NF:winuser.GetPointerType
title: GetPointerType function (winuser.h)
description: Retrieves the pointer type for a specified pointer.
helpviewer_keywords: ["GetPointerType","GetPointerType function [Input Messages and Notifications]","inputmsg.getpointertype","winuser/GetPointerType"]
old-location: inputmsg\getpointertype.htm
tech.root: InputMsg
ms.assetid: 63bfc340-9691-463c-96ca-0a5b80b8fe40
ms.date: 12/05/2018
ms.keywords: GetPointerType, GetPointerType function [Input Messages and Notifications], inputmsg.getpointertype, winuser/GetPointerType
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
 - GetPointerType
 - winuser/GetPointerType
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
 - GetPointerType
req.apiset: ext-ms-win-rtcore-ntuser-wmpointer-l1-1-0 (introduced in Windows 10, version 10.0.14393)
---

# GetPointerType function


## -description

Retrieves the pointer type for a specified pointer.

## -parameters

### -param pointerId [in]

An identifier of the pointer for which to retrieve pointer type.

### -param pointerType [out]

An address of a <a href="/windows/win32/api/winuser/ne-winuser-tagpointer_input_type">POINTER_INPUT_TYPE</a> type to receive a pointer input type.

## -returns

If the function succeeds, the return value is non-zero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

An application can use the <b>GetPointerType</b> function to determine the pointer type if it wishes to react differently to pointers of different types.

<div class="alert"><b>Note</b>  This function will never return with the generic <a href="/windows/win32/api/winuser/ne-winuser-tagpointer_input_type">PT_POINTER </a> type.</div>
<div> </div>

## -see-also

<a href="/windows/win32/inputmsg/functions">Functions</a>
