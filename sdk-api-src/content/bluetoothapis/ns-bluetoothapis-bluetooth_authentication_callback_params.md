---
UID: NS:bluetoothapis._BLUETOOTH_AUTHENTICATION_CALLBACK_PARAMS
title: BLUETOOTH_AUTHENTICATION_CALLBACK_PARAMS (bluetoothapis.h)
description: BLUETOOTH_AUTHENTICATION_CALLBACK_PARAMS structure contains specific configuration information about the Bluetooth device responding to an authentication request.
helpviewer_keywords: ["*PBLUETOOTH_AUTHENTICATION_CALLBACK_PARAMS","BLUETOOTH_AUTHENTICATION_CALLBACK_PARAMS","BLUETOOTH_AUTHENTICATION_CALLBACK_PARAMS structure [Bluetooth]","PBLUETOOTH_AUTHENTICATION_CALLBACK_PARAMS","PBLUETOOTH_AUTHENTICATION_CALLBACK_PARAMS structure pointer [Bluetooth]","bluetooth.bluetooth_authentication_callback_params","bluetoothapis/BLUETOOTH_AUTHENTICATION_CALLBACK_PARAMS","bluetoothapis/PBLUETOOTH_AUTHENTICATION_CALLBACK_PARAMS"]
old-location: bluetooth\bluetooth_authentication_callback_params.htm
tech.root: bluetooth
ms.assetid: e9c703c1-7981-4c34-a96e-0123d3655e55
ms.date: 12/05/2018
ms.keywords: '*PBLUETOOTH_AUTHENTICATION_CALLBACK_PARAMS, BLUETOOTH_AUTHENTICATION_CALLBACK_PARAMS, BLUETOOTH_AUTHENTICATION_CALLBACK_PARAMS structure [Bluetooth], PBLUETOOTH_AUTHENTICATION_CALLBACK_PARAMS, PBLUETOOTH_AUTHENTICATION_CALLBACK_PARAMS structure pointer [Bluetooth], bluetooth.bluetooth_authentication_callback_params, bluetoothapis/BLUETOOTH_AUTHENTICATION_CALLBACK_PARAMS, bluetoothapis/PBLUETOOTH_AUTHENTICATION_CALLBACK_PARAMS'
req.header: bluetoothapis.h
req.include-header: Bthsdpdef.h, BluetoothAPIs.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
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
req.typenames: BLUETOOTH_AUTHENTICATION_CALLBACK_PARAMS, *PBLUETOOTH_AUTHENTICATION_CALLBACK_PARAMS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _BLUETOOTH_AUTHENTICATION_CALLBACK_PARAMS
 - bluetoothapis/_BLUETOOTH_AUTHENTICATION_CALLBACK_PARAMS
 - PBLUETOOTH_AUTHENTICATION_CALLBACK_PARAMS
 - bluetoothapis/PBLUETOOTH_AUTHENTICATION_CALLBACK_PARAMS
 - BLUETOOTH_AUTHENTICATION_CALLBACK_PARAMS
 - bluetoothapis/BLUETOOTH_AUTHENTICATION_CALLBACK_PARAMS
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
 - BLUETOOTH_AUTHENTICATION_CALLBACK_PARAMS
---

# BLUETOOTH_AUTHENTICATION_CALLBACK_PARAMS structure


## -description

The <b>BLUETOOTH_AUTHENTICATION_CALLBACK_PARAMS</b> structure contains specific configuration information about the Bluetooth device responding to an authentication request.

## -struct-fields

### -field deviceInfo

A <a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_info_struct">BLUETOOTH_DEVICE_INFO</a> structure that contains information about a Bluetooth device.

### -field authenticationMethod

A <a href="/windows/win32/api/bluetoothapis/ne-bluetoothapis-bluetooth_authentication_method">BLUETOOTH_AUTHENTICATION_METHOD</a> enumeration that defines the authentication method utilized by the Bluetooth device.

### -field ioCapability

A <a href="/windows/win32/api/bluetoothapis/ne-bluetoothapis-bluetooth_io_capability">BLUETOOTH_IO_CAPABILITY</a> enumeration that defines the input/output capabilities of the Bluetooth device.

### -field authenticationRequirements

A <a href="/windows/win32/api/bluetoothapis/ne-bluetoothapis-bluetooth_authentication_requirements">BLUETOOTH_AUTHENTICATION_REQUIREMENTS</a> specifies the 'Man in the Middle' protection required for authentication.

### -field Numeric_Value

A <b>ULONG</b> value used for Numeric Comparison authentication.

### -field Passkey

A <b>ULONG</b> value used as  the passkey used for authentication.

## -see-also

<a href="/windows/win32/api/bluetoothapis/ne-bluetoothapis-bluetooth_authentication_requirements">BLUETOOTH_AUTHENTICATION_REQUIREMENTS</a>



<a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_info_struct">BLUETOOTH_DEVICE_INFO</a>



<a href="/windows/win32/api/bluetoothapis/ne-bluetoothapis-bluetooth_io_capability">BLUETOOTH_IO_CAPABILITY</a>

