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

# _BTH_LE_GATT_CHARACTERISTIC_VALUE structure


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




<a href="https://msdn.microsoft.com/96AC4E49-76D7-47B5-93B9-64D574A28E0A">Bluetooth GATT Notification Callback Function</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh450796">BluetoothGATTGetCharacteristicValue</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh450806">BluetoothGATTSetCharacteristicValue</a>
 

 

