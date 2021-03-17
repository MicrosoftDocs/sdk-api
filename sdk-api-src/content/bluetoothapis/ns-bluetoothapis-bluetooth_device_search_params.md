---
UID: NS:bluetoothapis._BLUETOOTH_DEVICE_SEARCH_PARAMS
title: BLUETOOTH_DEVICE_SEARCH_PARAMS (bluetoothapis.h)
description: Specifies search criteria for Bluetooth device searches.
helpviewer_keywords: ["BLUETOOTH_DEVICE_SEARCH_PARAMS","BLUETOOTH_DEVICE_SEARCH_PARAMS structure [Bluetooth]","bluetooth.bluetooth_device_search_params","bluetoothapis/BLUETOOTH_DEVICE_SEARCH_PARAMS"]
old-location: bluetooth\bluetooth_device_search_params.htm
tech.root: bluetooth
ms.assetid: e267df61-d0f5-434f-b49c-6899c2abfa2a
ms.date: 12/05/2018
ms.keywords: BLUETOOTH_DEVICE_SEARCH_PARAMS, BLUETOOTH_DEVICE_SEARCH_PARAMS structure [Bluetooth], bluetooth.bluetooth_device_search_params, bluetoothapis/BLUETOOTH_DEVICE_SEARCH_PARAMS
req.header: bluetoothapis.h
req.include-header: Bthsdpdef.h, BluetoothAPIs.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: BLUETOOTH_DEVICE_SEARCH_PARAMS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _BLUETOOTH_DEVICE_SEARCH_PARAMS
 - bluetoothapis/_BLUETOOTH_DEVICE_SEARCH_PARAMS
 - BLUETOOTH_DEVICE_SEARCH_PARAMS
 - bluetoothapis/BLUETOOTH_DEVICE_SEARCH_PARAMS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - BluetoothAPIs.h
api_name:
 - BLUETOOTH_DEVICE_SEARCH_PARAMS
---

# BLUETOOTH_DEVICE_SEARCH_PARAMS structure


## -description

The <b>BLUETOOTH_DEVICE_SEARCH_PARAMS</b> structure specifies search criteria for Bluetooth device searches.

## -struct-fields

### -field dwSize

The size, in bytes, of the structure.

### -field fReturnAuthenticated

A value that specifies that the search should return authenticated Bluetooth devices.

### -field fReturnRemembered

A value that specifies that the search should return remembered Bluetooth devices.

### -field fReturnUnknown

A value that specifies that the search should return unknown Bluetooth devices.

### -field fReturnConnected

A value that specifies that the search should return connected Bluetooth devices.

### -field fIssueInquiry

A value that specifies that a new inquiry should be issued.

### -field cTimeoutMultiplier

A value that indicates the time out for the inquiry, expressed in increments of 1.28 seconds. For example, an inquiry of 12.8 seconds has a <b>cTimeoutMultiplier</b> value of 10. The maximum value for this member is 48. When a value greater than 48 is used, the calling function immediately fails and returns <b>E_INVALIDARG</b>.

### -field hRadio

A handle for the radio on which to perform the inquiry. Set to <b>NULL</b> to perform the inquiry on all local Bluetooth radios.

## -see-also

<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothdisplaydeviceproperties">BluetoothDisplayDeviceProperties</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothfinddeviceclose">BluetoothFindDeviceClose</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothfindfirstdevice">BluetoothFindFirstDevice</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothfindnextdevice">BluetoothFindNextDevice</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothgetdeviceinfo">BluetoothGetDeviceInfo</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothremovedevice">BluetoothRemoveDevice</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothupdatedevicerecord">BluetoothUpdateDeviceRecord</a>