---
UID: NS:bluetoothapis._BLUETOOTH_AUTHENTICATE_RESPONSE
title: BLUETOOTH_AUTHENTICATE_RESPONSE (bluetoothapis.h)
description: BLUETOOTH_AUTHENTICATE_RESPONSE structure contains information passed in response to a BTH_REMOTE_AUTHENTICATE_REQUEST event.
helpviewer_keywords: ["*PBLUETOOTH_AUTHENTICATE_RESPONSE","BLUETOOTH_AUTHENTICATE_RESPONSE","BLUETOOTH_AUTHENTICATE_RESPONSE structure [Bluetooth]","PBLUETOOTH_AUTHENTICATE_RESPONSE","PBLUETOOTH_AUTHENTICATE_RESPONSE structure pointer [Bluetooth]","bluetooth.bluetooth_authenticate_response","bluetoothapis/BLUETOOTH_AUTHENTICATE_RESPONSE","bluetoothapis/PBLUETOOTH_AUTHENTICATE_RESPONSE"]
old-location: bluetooth\bluetooth_authenticate_response.htm
tech.root: bluetooth
ms.assetid: fc7eda84-3e7b-49e9-a1a6-e1759c894e1a
ms.date: 12/05/2018
ms.keywords: '*PBLUETOOTH_AUTHENTICATE_RESPONSE, BLUETOOTH_AUTHENTICATE_RESPONSE, BLUETOOTH_AUTHENTICATE_RESPONSE structure [Bluetooth], PBLUETOOTH_AUTHENTICATE_RESPONSE, PBLUETOOTH_AUTHENTICATE_RESPONSE structure pointer [Bluetooth], bluetooth.bluetooth_authenticate_response, bluetoothapis/BLUETOOTH_AUTHENTICATE_RESPONSE, bluetoothapis/PBLUETOOTH_AUTHENTICATE_RESPONSE'
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
req.typenames: BLUETOOTH_AUTHENTICATE_RESPONSE, *PBLUETOOTH_AUTHENTICATE_RESPONSE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _BLUETOOTH_AUTHENTICATE_RESPONSE
 - bluetoothapis/_BLUETOOTH_AUTHENTICATE_RESPONSE
 - PBLUETOOTH_AUTHENTICATE_RESPONSE
 - bluetoothapis/PBLUETOOTH_AUTHENTICATE_RESPONSE
 - BLUETOOTH_AUTHENTICATE_RESPONSE
 - bluetoothapis/BLUETOOTH_AUTHENTICATE_RESPONSE
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
 - BLUETOOTH_AUTHENTICATE_RESPONSE
---

## -description

The <b>BLUETOOTH_AUTHENTICATE_RESPONSE</b> structure contains information passed in response to a BTH_REMOTE_AUTHENTICATE_REQUEST event.

## -struct-fields

### -field bthAddressRemote

A <a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_address_struct">BLUETOOTH_ADDRESS</a> structure that contains the address of the device requesting the authentication response.  

<div class="alert"><b>Note</b>  This information can be found in the <a href="/windows/desktop/api/bluetoothapis/ns-bluetoothapis-bluetooth_authentication_callback_params">PBLUETOOTH_AUTHENTICATION_CALLBACK PARAMS</a> structure retrieved from the callback.</div>
<div> </div>

### -field authMethod

A <a href="/windows/win32/api/bluetoothapis/ne-bluetoothapis-bluetooth_authentication_method">BLUETOOTH_AUTHENTICATION_METHOD</a> enumeration that defines the supported authentication method. 

<div class="alert"><b>Note</b>  This information can be found in the <a href="/windows/desktop/api/bluetoothapis/ns-bluetoothapis-bluetooth_authentication_callback_params">PBLUETOOTH_AUTHENTICATION_CALLBACK PARAMS</a> structure retrieved from the callback.</div>
<div> </div>

### -field pinInfo

One of the following structures must be used according to the authentication method defined in <i>authMethod</i>. For example, if  <b>BLUETOOTH_AUTHENTICATION_METHOD_LEGACY</b> is specified, the BLUETOOTH_PIN_INFO structure must be populated.  

Contains information for pin authentication.

### -field oobInfo

Contains out-of-band data used to authenticate the device.

### -field numericCompInfo

Contains information for numeric comparison authentication.

### -field passkeyInfo

Contains information for passkey authentication.

### -field negativeResponse

<b>TRUE</b> if the authentication request was rejected; otherwise <b>FALSE</b>.

## -see-also

<a href="/windows/win32/api/bluetoothapis/ne-bluetoothapis-bluetooth_authentication_method">BLUETOOTH_AUTHENTICATION_METHOD</a>