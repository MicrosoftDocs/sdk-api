---
UID: NF:winuser.GetPointerDeviceRects
title: GetPointerDeviceRects function (winuser.h)
description: Gets the x and y range for the pointer device (in himetric) and the x and y range (current resolution) for the display that the pointer device is mapped to.
helpviewer_keywords: ["GetPointerDeviceRects","GetPointerDeviceRects function","input_pointerdevice.getpointerdevicerects","unifiedinputstack.getpointerdevicerects","winuser/GetPointerDeviceRects"]
old-location: input_pointerdevice\getpointerdevicerects.htm
tech.root: controls
ms.assetid: a6586dec-6d57-4345-be56-89c7308c1097
ms.date: 12/05/2018
ms.keywords: GetPointerDeviceRects, GetPointerDeviceRects function, input_pointerdevice.getpointerdevicerects, unifiedinputstack.getpointerdevicerects, winuser/GetPointerDeviceRects
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
 - GetPointerDeviceRects
 - winuser/GetPointerDeviceRects
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
 - GetPointerDeviceRects
---

# GetPointerDeviceRects function


## -description

Gets the x and y range for the pointer device (in himetric) and the x and y range (current resolution) for the display that the pointer device is mapped to.

## -parameters

### -param device [in]

The handle to the pointer device.

### -param pointerDeviceRect [out]

The structure for retrieving the device's physical range data.

### -param displayRect [out]

The structure for retrieving the display resolution.

## -returns

TRUE if the function succeeds; otherwise, FALSE. If the function fails, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function for more information.

## -see-also

<a href="/previous-versions/windows/desktop/input_pointerdevice/functions">Functions</a>