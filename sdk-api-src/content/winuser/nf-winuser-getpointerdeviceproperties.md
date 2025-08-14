---
UID: NF:winuser.GetPointerDeviceProperties
title: GetPointerDeviceProperties function (winuser.h)
description: Gets device properties that aren't included in the POINTER_DEVICE_INFO structure.
helpviewer_keywords: ["GetPointerDeviceProperties","GetPointerDeviceProperties function","input_pointerdevice.getpointerdeviceproperties","unifiedinputstack.getpointerdeviceproperties","winuser/GetPointerDeviceProperties"]
old-location: input_pointerdevice\getpointerdeviceproperties.htm
tech.root: controls
ms.assetid: dbb81637-217a-49b1-9e81-2068cf4c0951
ms.date: 12/05/2018
ms.keywords: GetPointerDeviceProperties, GetPointerDeviceProperties function, input_pointerdevice.getpointerdeviceproperties, unifiedinputstack.getpointerdeviceproperties, winuser/GetPointerDeviceProperties
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
 - GetPointerDeviceProperties
 - winuser/GetPointerDeviceProperties
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
 - GetPointerDeviceProperties
---

# GetPointerDeviceProperties function


## -description

Gets  device properties that aren't included in the <a href="/windows/desktop/api/winuser/ns-winuser-pointer_device_info">POINTER_DEVICE_INFO</a> structure.

## -parameters

### -param device [in]

The pointer device to query properties from. 

A call to the <a href="/windows/desktop/api/winuser/nf-winuser-getpointerdevices">GetPointerDevices</a> function returns this handle in the <a href="/windows/desktop/api/winuser/ns-winuser-pointer_device_info">POINTER_DEVICE_INFO</a> structure.

### -param propertyCount [in, out]

The number  of properties. 

Returns the count that's written or needed if <i>pointerProperties</i> is NULL.

If this value is less than the number of properties that the pointer device supports and <i>pointerProperties</i> is not NULL, the function returns the actual number of properties in this variable and fails.

### -param pointerProperties [out, optional]

The array of properties.

## -returns

TRUE if the function succeeds; otherwise, FALSE. If the function fails, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function for more information.

## -see-also

<a href="/previous-versions/windows/desktop/input_pointerdevice/functions">Functions</a>