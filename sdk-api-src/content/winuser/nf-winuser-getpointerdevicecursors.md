---
UID: NF:winuser.GetPointerDeviceCursors
title: GetPointerDeviceCursors function (winuser.h)
description: Gets the cursor IDs that are mapped to the cursors associated with a pointer device.
helpviewer_keywords: ["GetPointerDeviceCursors","GetPointerDeviceCursors function","input_pointerdevice.getpointerdevicecursors","unifiedinputstack.getpointerdevicecursors","winuser/GetPointerDeviceCursors"]
old-location: input_pointerdevice\getpointerdevicecursors.htm
tech.root: controls
ms.assetid: 4dd25033-e63a-4fa9-89b9-bfcae4061a76
ms.date: 12/05/2018
ms.keywords: GetPointerDeviceCursors, GetPointerDeviceCursors function, input_pointerdevice.getpointerdevicecursors, unifiedinputstack.getpointerdevicecursors, winuser/GetPointerDeviceCursors
req.header: winuser.h
req.include-header: 
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
 - GetPointerDeviceCursors
 - winuser/GetPointerDeviceCursors
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - GetPointerDeviceCursors
---

# GetPointerDeviceCursors function


## -description

Gets the cursor IDs that are mapped to the cursors associated with a pointer device.

## -parameters

### -param device [in]

The device handle.

### -param cursorCount [in, out]

The number of cursors associated with the pointer device.

### -param deviceCursors [out, optional]

An array of <a href="/windows/desktop/api/winuser/ns-winuser-pointer_device_cursor_info">POINTER_DEVICE_CURSOR_INFO</a> structures that contain info about the cursors. If NULL, <i>cursorCount</i> returns the number of cursors associated with the pointer device.

## -returns

TRUE if the function succeeds; otherwise, FALSE. If the function fails, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function for more information.

## -see-also

<a href="/previous-versions/windows/desktop/input_pointerdevice/functions">Functions</a>