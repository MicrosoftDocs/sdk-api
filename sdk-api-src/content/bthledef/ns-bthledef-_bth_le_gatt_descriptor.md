---
UID: NS:bthledef._BTH_LE_GATT_DESCRIPTOR
title: "_BTH_LE_GATT_DESCRIPTOR"
author: windows-sdk-content
description: The BTH_LE_GATT_DESCRIPTOR structure describes a Bluetooth Low Energy (LE) generic attribute (GATT) profile descriptor.
old-location: bltooth\bth_le_gatt_descriptor.htm
tech.root: bltooth
ms.assetid: DE738ADA-AE8E-4679-887C-A6194E88386E
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PBTH_LE_GATT_DESCRIPTOR, BTH_LE_GATT_DESCRIPTOR, BTH_LE_GATT_DESCRIPTOR structure [Bluetooth Devices], PBTH_LE_GATT_DESCRIPTOR, PBTH_LE_GATT_DESCRIPTOR structure pointer [Bluetooth Devices], _BTH_LE_GATT_DESCRIPTOR, bltooth.bth_le_gatt_descriptor, bthledef/BTH_LE_GATT_DESCRIPTOR, bthledef/PBTH_LE_GATT_DESCRIPTOR"
ms.prod: windows
ms.technology: windows-sdk
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
 - BTH_LE_GATT_DESCRIPTOR
product: Windows
targetos: Windows
req.typenames: BTH_LE_GATT_DESCRIPTOR, *PBTH_LE_GATT_DESCRIPTOR
req.redist: 
---

# _BTH_LE_GATT_DESCRIPTOR structure


## -description


The BTH_LE_GATT_DESCRIPTOR structure describes a Bluetooth Low Energy (LE) generic attribute (GATT) profile descriptor.


## -struct-fields




### -field ServiceHandle

The handle to the Bluetooth LE GATT profile service.


### -field CharacteristicHandle

The handle to the Bluetooth LE GATT profile characteristic.


### -field DescriptorType

The type of the Bluetooth LE GATT descriptor.


### -field DescriptorUuid

The Universally Unique ID (UUID) of the Bluetooth LE GATT descriptor.


### -field AttributeHandle

The handle to the Bluetooth LE GATT profile attributes.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh450845(v=VS.85).aspx">BTH_LE_GATT_DESCRIPTOR_TYPE</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh450852(v=VS.85).aspx">BTH_LE_UUID</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh450798(v=VS.85).aspx">BluetoothGATTGetDescriptorValue</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh450797(v=VS.85).aspx">BluetoothGATTGetDescriptors</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh450807(v=VS.85).aspx">BluetoothGATTSetDescriptorValue</a>
 

 

