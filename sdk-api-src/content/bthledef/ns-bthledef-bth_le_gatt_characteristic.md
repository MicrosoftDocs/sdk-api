---
UID: NS:bthledef._BTH_LE_GATT_CHARACTERISTIC
title: BTH_LE_GATT_CHARACTERISTIC (bthledef.h)
author: windows-sdk-content
description: The BTH_LE_GATT_CHARACTERISTIC structure describes a Bluetooth Low Energy (LE) generic attribute (GATT) profile characteristic.
old-location: bltooth\bth_le_gatt_characteristic.htm
tech.root: bltooth
ms.assetid: BE96F588-28C5-46C8-AFC9-852D940051F2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: '*PBTH_LE_GATT_CHARACTERISTIC, BTH_LE_GATT_CHARACTERISTIC, BTH_LE_GATT_CHARACTERISTIC structure [Bluetooth Devices], PBTH_LE_GATT_CHARACTERISTIC, PBTH_LE_GATT_CHARACTERISTIC structure pointer [Bluetooth Devices], bltooth.bth_le_gatt_characteristic, bthledef/BTH_LE_GATT_CHARACTERISTIC, bthledef/PBTH_LE_GATT_CHARACTERISTIC'
ms.topic: struct
f1_keywords:
- bthledef/BTH_LE_GATT_CHARACTERISTIC
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
- BTH_LE_GATT_CHARACTERISTIC
product: Windows
targetos: Windows
req.typenames: BTH_LE_GATT_CHARACTERISTIC, *PBTH_LE_GATT_CHARACTERISTIC
req.redist: 
ms.custom: 19H1
---

# BTH_LE_GATT_CHARACTERISTIC structure


## -description


The BTH_LE_GATT_CHARACTERISTIC structure describes a Bluetooth Low Energy (LE) generic attribute (GATT) profile characteristic.


## -struct-fields




### -field ServiceHandle

The handle to the Bluetooth LE GATT profile service.


### -field CharacteristicUuid

The Universally Unique ID (UUID) of the characteristic.


### -field AttributeHandle

The handle to the Bluetooth LE GATT profile attributes.


### -field CharacteristicValueHandle

The handle to the Bluetooth LE GATT profile characteristic value.


### -field IsBroadcastable

The characteristic can be broadcast.


### -field IsReadable

The characteristic  can be read.


### -field IsWritable

The characteristic  can be written to.


### -field IsWritableWithoutResponse

The characteristic  can be written to without requiring a response.


### -field IsSignedWritable

The characteristic can be signed writable.


### -field IsNotifiable

The characteristic can be updated by the device through Handle Value Notifications, and the new value will be returned through the callback function registered via <a href="https://docs.microsoft.com/windows/desktop/api/bluetoothleapis/nf-bluetoothleapis-bluetoothgattregisterevent">BluetoothGATTRegisterEvent</a>.


### -field IsIndicatable

The characteristic can be updated by the device through Handle Value Indications, and the new value will be returned through the callback function registered via <a href="https://docs.microsoft.com/windows/desktop/api/bluetoothleapis/nf-bluetoothleapis-bluetoothgattregisterevent">BluetoothGATTRegisterEvent</a>.


### -field HasExtendedProperties

The characteristic  has extended properties, which will be presented through a Characteristic Extended Properties descriptor.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/bthledef/ns-bthledef-bth_le_uuid">BTH_LE_UUID</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bluetoothleapis/nf-bluetoothleapis-bluetoothgattgetcharacteristicvalue">BluetoothGATTGetCharacteristicValue</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bluetoothleapis/nf-bluetoothleapis-bluetoothgattgetcharacteristics">BluetoothGATTGetCharacteristics</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bluetoothleapis/nf-bluetoothleapis-bluetoothgattsetcharacteristicvalue">BluetoothGATTSetCharacteristicValue</a>
 

 

