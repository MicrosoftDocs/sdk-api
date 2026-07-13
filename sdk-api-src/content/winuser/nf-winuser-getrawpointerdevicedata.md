---
UID: NF:winuser.GetRawPointerDeviceData
title: GetRawPointerDeviceData function (winuser.h)
description: Gets the raw input data from the pointer device.
helpviewer_keywords: ["GetRawPointerDeviceData","GetRawPointerDeviceData function","input_pointerdevice.getrawpointerdevicedata","unifiedinputstack.getrawpointerdevicedata","winuser/GetRawPointerDeviceData"]
old-location: input_pointerdevice\getrawpointerdevicedata.htm
tech.root: controls
ms.assetid: 56b65cc9-9582-4c7f-81e8-0b0d45b4dc8b
ms.date: 12/05/2018
ms.keywords: GetRawPointerDeviceData, GetRawPointerDeviceData function, input_pointerdevice.getrawpointerdevicedata, unifiedinputstack.getrawpointerdevicedata, winuser/GetRawPointerDeviceData
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
 - GetRawPointerDeviceData
 - winuser/GetRawPointerDeviceData
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
 - GetRawPointerDeviceData
---

# GetRawPointerDeviceData function


## -description

Gets the raw input data  from the pointer device.

## -parameters

### -param pointerId [in]

An identifier of the pointer for which to retrieve information.

### -param historyCount [in]

The pointer history.

### -param propertiesCount [in]

Number of properties to retrieve.

### -param pProperties [in]

Array of <a href="/windows/desktop/api/winuser/ns-winuser-pointer_device_property">POINTER_DEVICE_PROPERTY</a> structures that contain raw data reported by the device.

### -param pValues [out]

The values for <i>pProperties</i>.

## -returns

TRUE if the function succeeds; otherwise, FALSE. If the function fails, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function for more information.

## -see-also

<a href="/previous-versions/windows/desktop/input_pointerdevice/functions">Functions</a>