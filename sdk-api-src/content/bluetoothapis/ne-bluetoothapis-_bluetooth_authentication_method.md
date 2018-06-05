---
UID: NE:bluetoothapis._BLUETOOTH_AUTHENTICATION_METHOD
title: "_BLUETOOTH_AUTHENTICATION_METHOD"
author: windows-sdk-content
description: BLUETOOTH_AUTHENTICATION_METHOD enumeration defines the supported authentication types during device pairing.
old-location: bluetooth\bluetooth_authentication_method.htm
old-project: Bluetooth
ms.assetid: 2374df2c-2f50-4a06-aaad-384d81b067c5
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: "*PBLUETOOTH_AUTHENTICATION_METHOD, BLUETOOTH_AUTHENTICATION_METHOD, BLUETOOTH_AUTHENTICATION_METHOD enumeration [Bluetooth], BLUETOOTH_AUTHENTICATION_METHOD_LEGACY, BLUETOOTH_AUTHENTICATION_METHOD_NUMERIC_COMPARISON, BLUETOOTH_AUTHENTICATION_METHOD_OOB, BLUETOOTH_AUTHENTICATION_METHOD_PASSKEY, BLUETOOTH_AUTHENTICATION_METHOD_PASSKEY_NOTIFICATION, _BLUETOOTH_AUTHENTICATION_METHOD, bluetooth.bluetooth_authentication_method, bluetoothapis/BLUETOOTH_AUTHENTICATION_METHOD, bluetoothapis/BLUETOOTH_AUTHENTICATION_METHOD_LEGACY, bluetoothapis/BLUETOOTH_AUTHENTICATION_METHOD_NUMERIC_COMPARISON, bluetoothapis/BLUETOOTH_AUTHENTICATION_METHOD_OOB, bluetoothapis/BLUETOOTH_AUTHENTICATION_METHOD_PASSKEY, bluetoothapis/BLUETOOTH_AUTHENTICATION_METHOD_PASSKEY_NOTIFICATION"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: BLUETOOTH_AUTHENTICATION_METHOD, *PBLUETOOTH_AUTHENTICATION_METHOD
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	BluetoothAPIs.h
api_name:
-	BLUETOOTH_AUTHENTICATION_METHOD
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _BLUETOOTH_AUTHENTICATION_METHOD enumeration


## -description


The <b>BLUETOOTH_AUTHENTICATION_METHOD</b> enumeration defines the supported authentication types during device pairing.


## -enum-fields




### -field BLUETOOTH_AUTHENTICATION_METHOD_LEGACY

The Bluetooth device supports authentication via a PIN.


### -field BLUETOOTH_AUTHENTICATION_METHOD_OOB

The Bluetooth device supports authentication via out-of-band data.


### -field BLUETOOTH_AUTHENTICATION_METHOD_NUMERIC_COMPARISON

The Bluetooth device supports authentication via numeric comparison.


### -field BLUETOOTH_AUTHENTICATION_METHOD_PASSKEY_NOTIFICATION

The Bluetooth device supports authentication via passkey notification.


### -field BLUETOOTH_AUTHENTICATION_METHOD_PASSKEY

The Bluetooth device supports authentication via  passkey.

