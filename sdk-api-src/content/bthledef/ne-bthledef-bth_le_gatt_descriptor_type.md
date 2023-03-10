---
UID: NE:bthledef._BTH_LE_GATT_DESCRIPTOR_TYPE
title: BTH_LE_GATT_DESCRIPTOR_TYPE (bthledef.h)
description: The BTH_LE_GATT_DESCRIPTOR_TYPE enumeration describes the different types of Bluetooth LE generic attributes (GATT).
helpviewer_keywords: ["*PBTH_LE_GATT_DESCRIPTOR_TYPE","BTH_LE_GATT_DESCRIPTOR_TYPE","BTH_LE_GATT_DESCRIPTOR_TYPE enumeration [Bluetooth Devices]","CharacteristicAggregateFormat","CharacteristicExtendedProperties","CharacteristicFormat","CharacteristicUserDescription","ClientCharacteristicConfiguration","CustomDescriptor","ServerCharacteristicConfiguration","bltooth.bth_le_gatt_descriptor_type","bthledef/BTH_LE_GATT_DESCRIPTOR_TYPE","bthledef/CharacteristicAggregateFormat","bthledef/CharacteristicExtendedProperties","bthledef/CharacteristicFormat","bthledef/CharacteristicUserDescription","bthledef/ClientCharacteristicConfiguration","bthledef/CustomDescriptor","bthledef/ServerCharacteristicConfiguration"]
old-location: bltooth\bth_le_gatt_descriptor_type.htm
tech.root: bltooth
ms.assetid: 323D649D-B381-4293-BE7C-64651862B9DB
ms.date: 12/05/2018
ms.keywords: '*PBTH_LE_GATT_DESCRIPTOR_TYPE, BTH_LE_GATT_DESCRIPTOR_TYPE, BTH_LE_GATT_DESCRIPTOR_TYPE enumeration [Bluetooth Devices], CharacteristicAggregateFormat, CharacteristicExtendedProperties, CharacteristicFormat, CharacteristicUserDescription, ClientCharacteristicConfiguration, CustomDescriptor, ServerCharacteristicConfiguration, bltooth.bth_le_gatt_descriptor_type, bthledef/BTH_LE_GATT_DESCRIPTOR_TYPE, bthledef/CharacteristicAggregateFormat, bthledef/CharacteristicExtendedProperties, bthledef/CharacteristicFormat, bthledef/CharacteristicUserDescription, bthledef/ClientCharacteristicConfiguration, bthledef/CustomDescriptor, bthledef/ServerCharacteristicConfiguration'
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
req.typenames: BTH_LE_GATT_DESCRIPTOR_TYPE, *PBTH_LE_GATT_DESCRIPTOR_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _BTH_LE_GATT_DESCRIPTOR_TYPE
 - bthledef/_BTH_LE_GATT_DESCRIPTOR_TYPE
 - PBTH_LE_GATT_DESCRIPTOR_TYPE
 - bthledef/PBTH_LE_GATT_DESCRIPTOR_TYPE
 - BTH_LE_GATT_DESCRIPTOR_TYPE
 - bthledef/BTH_LE_GATT_DESCRIPTOR_TYPE
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
 - BTH_LE_GATT_DESCRIPTOR_TYPE
---

# BTH_LE_GATT_DESCRIPTOR_TYPE enumeration


## -description

The BTH_LE_GATT_DESCRIPTOR_TYPE enumeration describes the different types of Bluetooth LE generic attributes (GATT).

## -enum-fields

### -field CharacteristicExtendedProperties

The characteristic value has additional properties that describe how it  can be used, or how it can be accessed.

### -field CharacteristicUserDescription

The characteristic value contains a UTF-8 string of variable size that is a user textual
description.

### -field ClientCharacteristicConfiguration

The characteristic value may be configured by the
client.

### -field ServerCharacteristicConfiguration

The characteristic value may be configured for the
server.

### -field CharacteristicFormat

The format of the characteristic value.

### -field CharacteristicAggregateFormat

The format of an aggregated characteristic value.

### -field CustomDescriptor

The characteristic value is customized.

## -see-also

<a href="/windows/desktop/api/bthledef/ns-bthledef-bth_le_gatt_descriptor">BTH_LE_GATT_DESCRIPTOR</a>



<a href="/windows/desktop/api/bthledef/ns-bthledef-bth_le_gatt_descriptor_value">BTH_LE_GATT_DESCRIPTOR_VALUE</a>