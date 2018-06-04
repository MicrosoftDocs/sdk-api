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

# _BTH_LE_GATT_CHARACTERISTIC structure


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

The characteristic can be updated by the device through Handle Value Notifications, and the new value will be returned through the callback function registered via <a href="https://msdn.microsoft.com/library/windows/hardware/hh450804">BluetoothGATTRegisterEvent</a>.


### -field IsIndicatable

The characteristic can be updated by the device through Handle Value Indications, and the new value will be returned through the callback function registered via <a href="https://msdn.microsoft.com/library/windows/hardware/hh450804">BluetoothGATTRegisterEvent</a>.


### -field HasExtendedProperties

The characteristic  has extended properties, which will be presented through a Characteristic Extended Properties descriptor.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/hh450852">BTH_LE_UUID</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh450796">BluetoothGATTGetCharacteristicValue</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh450795">BluetoothGATTGetCharacteristics</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh450806">BluetoothGATTSetCharacteristicValue</a>
 

 

