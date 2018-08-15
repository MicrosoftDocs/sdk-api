---
UID: NE:bluetoothapis._BLUETOOTH_AUTHENTICATION_REQUIREMENTS
title: "_BLUETOOTH_AUTHENTICATION_REQUIREMENTS"
author: windows-sdk-content
description: BLUETOOTH_AUTHENTICATION_REQUIREMENTS enumeration specifies the 'Man in the Middle' protection required for authentication.
old-location: bluetooth\bluetooth_authentication_requirements.htm
old-project: bluetooth
ms.assetid: 644372af-d613-4fd6-adcd-7faf0afb0033
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: AUTHENTICATION_REQUIREMENTS, AUTHENTICATION_REQUIREMENTS enumeration [Bluetooth], BLUETOOTH_AUTHENTICATION_REQUIREMENTS, BLUETOOTH_AUTHENTICATION_REQUIREMENTS enumeration [Bluetooth], MITMProtectionNotDefined, MITMProtectionNotRequired, MITMProtectionNotRequiredBonding, MITMProtectionNotRequiredGeneralBonding, MITMProtectionRequired, MITMProtectionRequiredBonding, MITMProtectionRequiredGeneralBonding, _AUTHENTICATION_REQUIREMENTS, _BLUETOOTH_AUTHENTICATION_REQUIREMENTS, bluetooth.bluetooth_authentication_requirements, bluetoothapis/BLUETOOTH_AUTHENTICATION_REQUIREMENTS, bluetoothapis/MITMProtectionNotDefined, bluetoothapis/MITMProtectionNotRequired, bluetoothapis/MITMProtectionNotRequiredBonding, bluetoothapis/MITMProtectionNotRequiredGeneralBonding, bluetoothapis/MITMProtectionRequired, bluetoothapis/MITMProtectionRequiredBonding, bluetoothapis/MITMProtectionRequiredGeneralBonding
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: bluetoothapis.h
req.include-header: Bthsdpdef.h, BluetoothAPIs.h
req.redist: 
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
tech.root: 
req.typenames: BLUETOOTH_AUTHENTICATION_REQUIREMENTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - BluetoothAPIs.h
api_name:
 - AUTHENTICATION_REQUIREMENTS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _BLUETOOTH_AUTHENTICATION_REQUIREMENTS enumeration


## -description


The <b>BLUETOOTH_AUTHENTICATION_REQUIREMENTS</b> enumeration specifies the 'Man in the Middle' protection required for authentication.
<div class="alert"><b>Note</b>  This enumeration is supported in Windows Vista SP2 and Windows 7.</div><div> </div>

## -enum-fields




### -field BLUETOOTH_MITM_ProtectionNotRequired


### -field BLUETOOTH_MITM_ProtectionRequired


### -field BLUETOOTH_MITM_ProtectionNotRequiredBonding


### -field BLUETOOTH_MITM_ProtectionRequiredBonding


### -field BLUETOOTH_MITM_ProtectionNotRequiredGeneralBonding


### -field BLUETOOTH_MITM_ProtectionRequiredGeneralBonding


### -field BLUETOOTH_MITM_ProtectionNotDefined




#### - MITMProtectionNotDefined

Protection against "Man in the Middle" attack is not defined.


#### - MITMProtectionNotRequired

Protection against a "Man in the Middle" attack is not required for authentication.


#### - MITMProtectionNotRequiredBonding

Protection against a "Man in the Middle" attack is not required for bonding.


#### - MITMProtectionNotRequiredGeneralBonding

Protection against a "Man in the Middle" attack is not required for General Bonding.


#### - MITMProtectionRequired

Protection against a "Man in the Middle" attack is required for authentication.


#### - MITMProtectionRequiredBonding

Protection against a "Man in the Middle" attack is required for bonding.


#### - MITMProtectionRequiredGeneralBonding

Protection against a "Man in the Middle" attack is required for General Bonding.


## -remarks



The header file associated with this API is available at Microsoft Connect via the Windows Vista Feature Pack for Wireless Developers Supplement download. Access to this resource requires registration with the Microsoft Connect website. The header is also included in the comprehensive developer resource packages available via the Windows Driver Kit (WDK), Windows Logo Kit (WLK) and Windows Driver Framework (WDF) Connections at Microsoft Connect. 




## -see-also




<a href="https://msdn.microsoft.com/948bf14c-9661-4fe9-b082-009afd867baf">BluetoothAuthenticateDeviceEx</a>
 

 

