---
UID: NS:bthledef._BTH_LE_GATT_DESCRIPTOR_VALUE
title: "_BTH_LE_GATT_DESCRIPTOR_VALUE"
author: windows-driver-content
description: The BTH_LE_GATT_DESCRIPTOR_VALUE structure describes a parent characteristic.
old-location: bltooth\bth_le_gatt_descriptor_value.htm
old-project: bltooth
ms.assetid: 81D05AA7-B16C-4705-919F-8563FFA4A58E
ms.author: windowsdriverdev
ms.date: 4/27/2018
ms.keywords: "*PBTH_LE_GATT_DESCRIPTOR_VALUE, BTH_LE_GATT_DESCRIPTOR_VALUE, BTH_LE_GATT_DESCRIPTOR_VALUE structure [Bluetooth Devices], PBTH_LE_GATT_DESCRIPTOR_VALUE, PBTH_LE_GATT_DESCRIPTOR_VALUE structure pointer [Bluetooth Devices], _BTH_LE_GATT_DESCRIPTOR_VALUE, bltooth.bth_le_gatt_descriptor_value, bthledef/BTH_LE_GATT_DESCRIPTOR_VALUE, bthledef/PBTH_LE_GATT_DESCRIPTOR_VALUE"
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
req.typenames: BTH_LE_GATT_DESCRIPTOR_VALUE, *PBTH_LE_GATT_DESCRIPTOR_VALUE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	BthLEDef.h
api_name:
-	BTH_LE_GATT_DESCRIPTOR_VALUE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _BTH_LE_GATT_DESCRIPTOR_VALUE structure


## -description


The BTH_LE_GATT_DESCRIPTOR_VALUE structure describes a parent characteristic.


## -struct-fields




### -field DescriptorType

The type of the descriptor value.


### -field DescriptorUuid

The Universally Unique ID (UUID) of the descriptor value.


### -field CharacteristicExtendedProperties

Container structure for the different characteristic extended property members.


### -field CharacteristicExtendedProperties.IsReliableWriteEnabled

The parent characteristic value is reliable write enabled.


### -field CharacteristicExtendedProperties.IsAuxiliariesWritable

The characteristic user description descriptor is writable.


### -field CharacteristicExtendedProperties.case

 


### -field CharacteristicExtendedProperties.case.CharacteristicExtendedProperties

 


### -field ClientCharacteristicConfiguration

Container structure for the different client characteristic configuration members.


### -field ClientCharacteristicConfiguration.IsSubscribeToNotification

Whether the characteristic has been registered with the device to receive Handle Value Notifications. TRUE if the characteristic has been registered. Otherwise, FALSE.


### -field ClientCharacteristicConfiguration.IsSubscribeToIndication

Whether the characteristic has been registered with the device to receive Handle Value Indications. TRUE if the characteristic has been registered. Otherwise, FALSE.


### -field ClientCharacteristicConfiguration.case

 


### -field ClientCharacteristicConfiguration.case.ClientCharacteristicConfiguration

 


### -field ServerCharacteristicConfiguration

Container structure for the different server characteristic configuration members.


### -field ServerCharacteristicConfiguration.IsBroadcast

The parent characteristic value can be broadcast.


### -field ServerCharacteristicConfiguration.case

 


### -field ServerCharacteristicConfiguration.case.ServerCharacteristicConfiguration

 


### -field CharacteristicFormat

Container structure for the different characteristic format members.


### -field CharacteristicFormat.Format

The format of the parent characteristic value.


### -field CharacteristicFormat.Exponent

The exponent value to use to determine how the value of the characteristic value is further formatted.


### -field CharacteristicFormat.Unit

The unit of the characteristic value as defined in the Assigned Numbers specification.


### -field CharacteristicFormat.NameSpace

The name-space where the unit is defined in the Assigned Numbers specification.


### -field CharacteristicFormat.Description

The Universally Unique ID (UUID) that describes the format of the parent characteristic value.


### -field CharacteristicFormat.case

 


### -field CharacteristicFormat.case.CharacteristicFormat

 


### -field switch_type

 


### -field switch_type.BTH_LE_GATT_DESCRIPTOR_TYPE

 


### -field switch_is

 


### -field switch_is.(BTH_LE_GATT_DESCRIPTOR_TYPE)DescriptorType

 


### -field DataSize

The size, in bytes, of the descriptor value.


### -field Data.size_is

 


### -field Data.size_is.DataSize

 


### -field Data

 




#### - Data[]

A pointer to the descriptor value data.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/hh450845">BTH_LE_GATT_DESCRIPTOR_TYPE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh450852">BTH_LE_UUID</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh450798">BluetoothGATTGetDescriptorValue</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh450807">BluetoothGATTSetDescriptorValue</a>
 

 

