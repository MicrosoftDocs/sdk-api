---
UID: NS:bthledef._BTH_LE_GATT_CHARACTERISTIC_VALUE
title: "_BTH_LE_GATT_CHARACTERISTIC_VALUE"
author: windows-sdk-content
description: The BTH_LE_GATT_CHARACTERISTIC_VALUE structure describes a Bluetooth Low Energy (LE) generic attribute (GATT) profile characteristic value.
old-location: bltooth\bth_le_gatt_characteristic_value.htm
tech.root: bltooth
ms.assetid: AF36BC9A-5EB7-4495-870A-40BF5E0A57A3
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PBTH_LE_GATT_CHARACTERISTIC_VALUE, BTH_LE_GATT_CHARACTERISTIC_VALUE, BTH_LE_GATT_CHARACTERISTIC_VALUE structure [Bluetooth Devices], PBTH_LE_GATT_CHARACTERISTIC_VALUE, PBTH_LE_GATT_CHARACTERISTIC_VALUE structure pointer [Bluetooth Devices], _BTH_LE_GATT_CHARACTERISTIC_VALUE, bltooth.bth_le_gatt_characteristic_value, bthledef/BTH_LE_GATT_CHARACTERISTIC_VALUE, bthledef/PBTH_LE_GATT_CHARACTERISTIC_VALUE"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: BTH_LE_GATT_CHARACTERISTIC_VALUE, *PBTH_LE_GATT_CHARACTERISTIC_VALUE
req.redist: 
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




<a href="https://msdn.microsoft.com/en-us/library/Hh450822(v=VS.85).aspx">Bluetooth GATT Notification Callback Function</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh450796(v=VS.85).aspx">BluetoothGATTGetCharacteristicValue</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh450806(v=VS.85).aspx">BluetoothGATTSetCharacteristicValue</a>
 

 

