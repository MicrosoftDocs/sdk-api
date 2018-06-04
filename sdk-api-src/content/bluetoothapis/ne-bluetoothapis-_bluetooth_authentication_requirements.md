---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

