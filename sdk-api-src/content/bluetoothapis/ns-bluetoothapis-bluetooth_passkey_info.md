---
UID: NS:bluetoothapis._BLUETOOTH_PASSKEY_INFO
title: BLUETOOTH_PASSKEY_INFO (bluetoothapis.h)
description: BLUETOOTH_PASSKEY_INFO structure contains a passkey value used for authentication. A passkey is similar to a password, except that a passkey value is used for authentication only once.
helpviewer_keywords: ["*PBLUETOOTH_PASSKEY_INFO","BLUETOOTH_PASSKEY_INFO","BLUETOOTH_PASSKEY_INFO structure [Bluetooth]","PBLUETOOTH_PASSKEY_INFO","PBLUETOOTH_PASSKEY_INFO structure pointer [Bluetooth]","bluetooth.bluetooth_passkey_info","bluetoothapis/BLUETOOTH_PASSKEY_INFO","bluetoothapis/PBLUETOOTH_PASSKEY_INFO"]
old-location: bluetooth\bluetooth_passkey_info.htm
tech.root: bluetooth
ms.assetid: 18f4c26a-7d71-4af0-a8df-a7722028ff62
ms.date: 12/05/2018
ms.keywords: '*PBLUETOOTH_PASSKEY_INFO, BLUETOOTH_PASSKEY_INFO, BLUETOOTH_PASSKEY_INFO structure [Bluetooth], PBLUETOOTH_PASSKEY_INFO, PBLUETOOTH_PASSKEY_INFO structure pointer [Bluetooth], bluetooth.bluetooth_passkey_info, bluetoothapis/BLUETOOTH_PASSKEY_INFO, bluetoothapis/PBLUETOOTH_PASSKEY_INFO'
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
req.typenames: BLUETOOTH_PASSKEY_INFO, *PBLUETOOTH_PASSKEY_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _BLUETOOTH_PASSKEY_INFO
 - bluetoothapis/_BLUETOOTH_PASSKEY_INFO
 - PBLUETOOTH_PASSKEY_INFO
 - bluetoothapis/PBLUETOOTH_PASSKEY_INFO
 - BLUETOOTH_PASSKEY_INFO
 - bluetoothapis/BLUETOOTH_PASSKEY_INFO
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
 - BLUETOOTH_PASSKEY_INFO
---

# BLUETOOTH_PASSKEY_INFO structure


## -description

The <b>BLUETOOTH_PASSKEY_INFO</b> structure contains a passkey  value used  for authentication.  A passkey is similar to a password, except that a passkey value is used for authentication only once.

## -struct-fields

### -field passkey

The passkey used for authentication.

## -see-also

<a href="/windows/desktop/api/bluetoothapis/ne-bluetoothapis-bluetooth_authentication_method">BLUETOOTH_AUTHENTICATION_METHODS</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothauthenticatedevice">BluetoothAuthenticateDevice</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothauthenticatedeviceex">BluetoothAuthenticateDeviceEx</a>