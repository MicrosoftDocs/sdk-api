---
UID: NF:winuser.GetPointerCursorId
title: GetPointerCursorId function (winuser.h)
description: Retrieves the cursor identifier associated with the specified pointer.
helpviewer_keywords: ["GetPointerCursorId","GetPointerCursorId function [Input Messages and Notifications]","inputmsg.getpointercursorid","winuser/GetPointerCursorId"]
old-location: inputmsg\getpointercursorid.htm
tech.root: InputMsg
ms.assetid: 43211600-ee82-416f-860f-423c581eda75
ms.date: 12/05/2018
ms.keywords: GetPointerCursorId, GetPointerCursorId function [Input Messages and Notifications], inputmsg.getpointercursorid, winuser/GetPointerCursorId
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
 - GetPointerCursorId
 - winuser/GetPointerCursorId
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
 - GetPointerCursorId
---

# GetPointerCursorId function


## -description

Retrieves the cursor identifier associated with the specified pointer.

## -parameters

### -param pointerId [in]

An identifier of the pointer for which to retrieve the cursor identifier.

### -param cursorId [out]

An address of a <b>UINT32</b> to receive the tablet cursor identifier, if any, associated with the specified pointer.

## -returns

If the function succeeds, the return value is non-zero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Cursor objects represent pointing and selecting devices used with digitizer devices, most commonly tactile contacts on touch digitizers and tablet pens on pen digitizers. Physical pens may have multiple tips (such as normal and eraser ends), with each pen tip representing a different cursor object. Each cursor object has an associated cursor identifier.

For pointer types that derive from these cursor objects, an application can use the <b>GetPointerCursorId</b> function to retrieve the cursor identifier associated with a pointer.

## -see-also

<a href="/windows/win32/inputmsg/functions">Functions</a>