---
UID: NE:bluetoothapis._BLUETOOTH_AUTHENTICATION_REQUIREMENTS
title: BLUETOOTH_AUTHENTICATION_REQUIREMENTS (bluetoothapis.h)
description: BLUETOOTH_AUTHENTICATION_REQUIREMENTS enumeration specifies the 'Man in the Middle' protection required for authentication.
helpviewer_keywords: ["BLUETOOTH_AUTHENTICATION_REQUIREMENTS","BLUETOOTH_AUTHENTICATION_REQUIREMENTS enumeration [Bluetooth]","BLUETOOTH_MITM_ProtectionNotDefined","BLUETOOTH_MITM_ProtectionNotRequired","BLUETOOTH_MITM_ProtectionNotRequiredBonding","BLUETOOTH_MITM_ProtectionRequired","BLUETOOTH_MITM_ProtectionRequiredBonding","BLUETOOTH_MITM_ProtectionRequiredGeneralBonding","MBLUETOOTH_MITM_ProtectionNotRequiredGeneralBonding","_BLUETOOTH_AUTHENTICATION_REQUIREMENTS","bluetooth.bluetooth_authentication_requirements","bluetoothapis/BLUETOOTH_AUTHENTICATION_REQUIREMENTS","bluetoothapis/BLUETOOTH_MITM_ProtectionNotDefined","bluetoothapis/BLUETOOTH_MITM_ProtectionNotRequired","bluetoothapis/BLUETOOTH_MITM_ProtectionNotRequiredBonding","bluetoothapis/BLUETOOTH_MITM_ProtectionRequired","bluetoothapis/BLUETOOTH_MITM_ProtectionRequiredBonding","bluetoothapis/BLUETOOTH_MITM_ProtectionRequiredGeneralBonding","bluetoothapis/MBLUETOOTH_MITM_ProtectionNotRequiredGeneralBonding"]
old-location: bluetooth\bluetooth_authentication_requirements.htm
tech.root: bluetooth
ms.assetid: 644372af-d613-4fd6-adcd-7faf0afb0033
ms.date: 12/05/2018
ms.keywords: BLUETOOTH_AUTHENTICATION_REQUIREMENTS, BLUETOOTH_AUTHENTICATION_REQUIREMENTS enumeration [Bluetooth], BLUETOOTH_MITM_ProtectionNotDefined, BLUETOOTH_MITM_ProtectionNotRequired, BLUETOOTH_MITM_ProtectionNotRequiredBonding, BLUETOOTH_MITM_ProtectionRequired, BLUETOOTH_MITM_ProtectionRequiredBonding, BLUETOOTH_MITM_ProtectionRequiredGeneralBonding, MBLUETOOTH_MITM_ProtectionNotRequiredGeneralBonding, _BLUETOOTH_AUTHENTICATION_REQUIREMENTS, bluetooth.bluetooth_authentication_requirements, bluetoothapis/BLUETOOTH_AUTHENTICATION_REQUIREMENTS, bluetoothapis/BLUETOOTH_MITM_ProtectionNotDefined, bluetoothapis/BLUETOOTH_MITM_ProtectionNotRequired, bluetoothapis/BLUETOOTH_MITM_ProtectionNotRequiredBonding, bluetoothapis/BLUETOOTH_MITM_ProtectionRequired, bluetoothapis/BLUETOOTH_MITM_ProtectionRequiredBonding, bluetoothapis/BLUETOOTH_MITM_ProtectionRequiredGeneralBonding, bluetoothapis/MBLUETOOTH_MITM_ProtectionNotRequiredGeneralBonding
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
req.typenames: BLUETOOTH_AUTHENTICATION_REQUIREMENTS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _BLUETOOTH_AUTHENTICATION_REQUIREMENTS
 - bluetoothapis/_BLUETOOTH_AUTHENTICATION_REQUIREMENTS
 - BLUETOOTH_AUTHENTICATION_REQUIREMENTS
 - bluetoothapis/BLUETOOTH_AUTHENTICATION_REQUIREMENTS
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
 - BLUETOOTH_AUTHENTICATION_REQUIREMENTS
---

## -description

The <b>BLUETOOTH_AUTHENTICATION_REQUIREMENTS</b> enumeration specifies the 'Man in the Middle' protection required for authentication.
<div class="alert"><b>Note</b>  This enumeration is supported in Windows Vista SP2 and Windows 7.</div><div> </div>

## -enum-fields

### -field BLUETOOTH_MITM_ProtectionNotRequired:0

Protection against a "Man in the Middle" attack is not required for authentication.

### -field BLUETOOTH_MITM_ProtectionRequired:0x1

Protection against a "Man in the Middle" attack is required for authentication.

### -field BLUETOOTH_MITM_ProtectionNotRequiredBonding:0x2

Protection against a "Man in the Middle" attack is not required for bonding.

### -field BLUETOOTH_MITM_ProtectionRequiredBonding:0x3

Protection against a "Man in the Middle" attack is required for bonding.

### -field BLUETOOTH_MITM_ProtectionNotRequiredGeneralBonding:0x4

Protection against a "Man in the Middle" attack is not required for General Bonding.

### -field BLUETOOTH_MITM_ProtectionRequiredGeneralBonding:0x5

Protection against a "Man in the Middle" attack is required for General Bonding.

### -field BLUETOOTH_MITM_ProtectionNotDefined:0xff

Protection against "Man in the Middle" attack is not defined.

## -remarks

The header file associated with this API is available at Microsoft Connect via the Windows Vista Feature Pack for Wireless Developers Supplement download. Access to this resource requires registration with the Microsoft Connect website. The header is also included in the comprehensive developer resource packages available via the Windows Driver Kit (WDK), Windows Logo Kit (WLK) and Windows Driver Framework (WDF) Connections at Microsoft Connect.

## -see-also

<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothauthenticatedeviceex">BluetoothAuthenticateDeviceEx</a>
