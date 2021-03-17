---
UID: NS:bthledef._BTH_LE_GATT_DESCRIPTOR_VALUE
title: BTH_LE_GATT_DESCRIPTOR_VALUE (bthledef.h)
description: The BTH_LE_GATT_DESCRIPTOR_VALUE structure describes a parent characteristic.
helpviewer_keywords: ["*PBTH_LE_GATT_DESCRIPTOR_VALUE","BTH_LE_GATT_DESCRIPTOR_VALUE","BTH_LE_GATT_DESCRIPTOR_VALUE structure [Bluetooth Devices]","PBTH_LE_GATT_DESCRIPTOR_VALUE","PBTH_LE_GATT_DESCRIPTOR_VALUE structure pointer [Bluetooth Devices]","bltooth.bth_le_gatt_descriptor_value","bthledef/BTH_LE_GATT_DESCRIPTOR_VALUE","bthledef/PBTH_LE_GATT_DESCRIPTOR_VALUE"]
old-location: bltooth\bth_le_gatt_descriptor_value.htm
tech.root: bltooth
ms.assetid: 81D05AA7-B16C-4705-919F-8563FFA4A58E
ms.date: 12/05/2018
ms.keywords: '*PBTH_LE_GATT_DESCRIPTOR_VALUE, BTH_LE_GATT_DESCRIPTOR_VALUE, BTH_LE_GATT_DESCRIPTOR_VALUE structure [Bluetooth Devices], PBTH_LE_GATT_DESCRIPTOR_VALUE, PBTH_LE_GATT_DESCRIPTOR_VALUE structure pointer [Bluetooth Devices], bltooth.bth_le_gatt_descriptor_value, bthledef/BTH_LE_GATT_DESCRIPTOR_VALUE, bthledef/PBTH_LE_GATT_DESCRIPTOR_VALUE'
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
targetos: Windows
req.typenames: BTH_LE_GATT_DESCRIPTOR_VALUE, *PBTH_LE_GATT_DESCRIPTOR_VALUE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _BTH_LE_GATT_DESCRIPTOR_VALUE
 - bthledef/_BTH_LE_GATT_DESCRIPTOR_VALUE
 - PBTH_LE_GATT_DESCRIPTOR_VALUE
 - bthledef/PBTH_LE_GATT_DESCRIPTOR_VALUE
 - BTH_LE_GATT_DESCRIPTOR_VALUE
 - bthledef/BTH_LE_GATT_DESCRIPTOR_VALUE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - BthLEDef.h
api_name:
 - BTH_LE_GATT_DESCRIPTOR_VALUE
---

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

### -field ClientCharacteristicConfiguration

Container structure for the different client characteristic configuration members.

### -field ClientCharacteristicConfiguration.IsSubscribeToNotification

Whether the characteristic has been registered with the device to receive Handle Value Notifications. TRUE if the characteristic has been registered. Otherwise, FALSE.

### -field ClientCharacteristicConfiguration.IsSubscribeToIndication

Whether the characteristic has been registered with the device to receive Handle Value Indications. TRUE if the characteristic has been registered. Otherwise, FALSE.

### -field ServerCharacteristicConfiguration

Container structure for the different server characteristic configuration members.

### -field ServerCharacteristicConfiguration.IsBroadcast

The parent characteristic value can be broadcast.

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

### -field DataSize

The size, in bytes, of the descriptor value.

### -field Data

A pointer to the descriptor value data.

## -see-also

<a href="/windows/desktop/api/bthledef/ne-bthledef-bth_le_gatt_descriptor_type">BTH_LE_GATT_DESCRIPTOR_TYPE</a>

<a href="/windows/desktop/api/bthledef/ns-bthledef-bth_le_uuid">BTH_LE_UUID</a>

<a href="/windows/desktop/api/bluetoothleapis/nf-bluetoothleapis-bluetoothgattgetdescriptorvalue">BluetoothGATTGetDescriptorValue</a>

<a href="/windows/desktop/api/bluetoothleapis/nf-bluetoothleapis-bluetoothgattsetdescriptorvalue">BluetoothGATTSetDescriptorValue</a>