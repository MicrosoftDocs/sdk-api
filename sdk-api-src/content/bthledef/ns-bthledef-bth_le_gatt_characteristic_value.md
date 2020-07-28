---
UID: NS:bthledef._BTH_LE_GATT_CHARACTERISTIC_VALUE
title: BTH_LE_GATT_CHARACTERISTIC_VALUE (bthledef.h)
description: The BTH_LE_GATT_CHARACTERISTIC_VALUE structure describes a Bluetooth Low Energy (LE) generic attribute (GATT) profile characteristic value.
helpviewer_keywords: ["*PBTH_LE_GATT_CHARACTERISTIC_VALUE","BTH_LE_GATT_CHARACTERISTIC_VALUE","BTH_LE_GATT_CHARACTERISTIC_VALUE structure [Bluetooth Devices]","PBTH_LE_GATT_CHARACTERISTIC_VALUE","PBTH_LE_GATT_CHARACTERISTIC_VALUE structure pointer [Bluetooth Devices]","bltooth.bth_le_gatt_characteristic_value","bthledef/BTH_LE_GATT_CHARACTERISTIC_VALUE","bthledef/PBTH_LE_GATT_CHARACTERISTIC_VALUE"]
old-location: bltooth\bth_le_gatt_characteristic_value.htm
tech.root: bltooth
ms.assetid: AF36BC9A-5EB7-4495-870A-40BF5E0A57A3
ms.date: 12/05/2018
ms.keywords: '*PBTH_LE_GATT_CHARACTERISTIC_VALUE, BTH_LE_GATT_CHARACTERISTIC_VALUE, BTH_LE_GATT_CHARACTERISTIC_VALUE structure [Bluetooth Devices], PBTH_LE_GATT_CHARACTERISTIC_VALUE, PBTH_LE_GATT_CHARACTERISTIC_VALUE structure pointer [Bluetooth Devices], bltooth.bth_le_gatt_characteristic_value, bthledef/BTH_LE_GATT_CHARACTERISTIC_VALUE, bthledef/PBTH_LE_GATT_CHARACTERISTIC_VALUE'
f1_keywords:
- bthledef/BTH_LE_GATT_CHARACTERISTIC_VALUE
dev_langs:
- c++
req.header: bthledef.h
req.include-header: BthLEDef.h
req.target-type: Windows
req.target-min-winverclnt: Versions:\_Supported in Windows 8
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- BthLEDef.h
api_name:
- BTH_LE_GATT_CHARACTERISTIC_VALUE
targetos: Windows
req.typenames: BTH_LE_GATT_CHARACTERISTIC_VALUE, *PBTH_LE_GATT_CHARACTERISTIC_VALUE
req.redist: 
ms.custom: 19H1
---

# BTH_LE_GATT_CHARACTERISTIC_VALUE structure


## -description


The BTH_LE_GATT_CHARACTERISTIC_VALUE structure describes a Bluetooth Low Energy (LE) generic attribute (GATT) profile characteristic value.


## -struct-fields




### -field DataSize

The size, in bytes, of the Bluetooth LE GATT characteristic value.


### -field Data.size_is

 


### -field Data.size_is.DataSize

 


### -field Data

 




#### - Data[]

A pointer to the Bluetooth LE GATT characteristic value data.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/bthledef/nc-bthledef-pfnbluetooth_gatt_event_callback">Bluetooth GATT Notification Callback Function</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bluetoothleapis/nf-bluetoothleapis-bluetoothgattgetcharacteristicvalue">BluetoothGATTGetCharacteristicValue</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bluetoothleapis/nf-bluetoothleapis-bluetoothgattsetcharacteristicvalue">BluetoothGATTSetCharacteristicValue</a>
 

 

