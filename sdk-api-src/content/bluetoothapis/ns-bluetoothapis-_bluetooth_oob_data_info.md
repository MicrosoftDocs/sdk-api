---
UID: NS:bluetoothapis._BLUETOOTH_OOB_DATA_INFO
title: "_BLUETOOTH_OOB_DATA_INFO"
author: windows-sdk-content
description: BLUETOOTH_OOB_DATA_INFO structure contains data used to authenticate prior to establishing an Out-of-Band device pairing.
old-location: bluetooth\bluetooth_oob_data_info.htm
tech.root: Bluetooth
ms.assetid: 0728678a-98c7-44b5-a117-5f9acae9fd25
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PBLUETOOTH_OOB_DATA_INFO, BLUETOOTH_OOB_DATA_INFO, BLUETOOTH_OOB_DATA_INFO structure [Bluetooth], PBLUETOOTH_OOB_DATA_INFO, PBLUETOOTH_OOB_DATA_INFO structure pointer [Bluetooth], _BLUETOOTH_OOB_DATA_INFO, bluetooth.bluetooth_oob_data_info, bluetoothapis/BLUETOOTH_OOB_DATA_INFO, bluetoothapis/PBLUETOOTH_OOB_DATA_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - BluetoothAPIs.h
api_name:
 - BLUETOOTH_OOB_DATA_INFO
product: Windows
targetos: Windows
req.typenames: BLUETOOTH_OOB_DATA_INFO, *PBLUETOOTH_OOB_DATA_INFO
req.redist: 
---

# _BLUETOOTH_OOB_DATA_INFO structure


## -description


The <b>BLUETOOTH_OOB_DATA_INFO</b> structure contains data used to authenticate prior to establishing an Out-of-Band device pairing.


## -struct-fields




### -field C

A 128-bit cryptographic key used for two-way authentication.


### -field R

A randomly generated number used for one-way authentication. If this number is not provided by the device initiating the OOB session, this value is 0.


## -remarks



For more details regarding the creation of keys for OOB authentication, see the <a href="http://go.microsoft.com/fwlink/p/?linkid=178090">Bluetooth Core Specification</a>.



