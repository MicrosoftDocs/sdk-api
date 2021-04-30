---
UID: NS:bthledef._BTH_LE_GATT_DESCRIPTOR
title: BTH_LE_GATT_DESCRIPTOR (bthledef.h)
description: The BTH_LE_GATT_DESCRIPTOR structure describes a Bluetooth Low Energy (LE) generic attribute (GATT) profile descriptor.
helpviewer_keywords: ["*PBTH_LE_GATT_DESCRIPTOR","BTH_LE_GATT_DESCRIPTOR","BTH_LE_GATT_DESCRIPTOR structure [Bluetooth Devices]","PBTH_LE_GATT_DESCRIPTOR","PBTH_LE_GATT_DESCRIPTOR structure pointer [Bluetooth Devices]","bltooth.bth_le_gatt_descriptor","bthledef/BTH_LE_GATT_DESCRIPTOR","bthledef/PBTH_LE_GATT_DESCRIPTOR"]
old-location: bltooth\bth_le_gatt_descriptor.htm
tech.root: bltooth
ms.assetid: DE738ADA-AE8E-4679-887C-A6194E88386E
ms.date: 12/05/2018
ms.keywords: '*PBTH_LE_GATT_DESCRIPTOR, BTH_LE_GATT_DESCRIPTOR, BTH_LE_GATT_DESCRIPTOR structure [Bluetooth Devices], PBTH_LE_GATT_DESCRIPTOR, PBTH_LE_GATT_DESCRIPTOR structure pointer [Bluetooth Devices], bltooth.bth_le_gatt_descriptor, bthledef/BTH_LE_GATT_DESCRIPTOR, bthledef/PBTH_LE_GATT_DESCRIPTOR'
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
req.typenames: BTH_LE_GATT_DESCRIPTOR, *PBTH_LE_GATT_DESCRIPTOR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _BTH_LE_GATT_DESCRIPTOR
 - bthledef/_BTH_LE_GATT_DESCRIPTOR
 - PBTH_LE_GATT_DESCRIPTOR
 - bthledef/PBTH_LE_GATT_DESCRIPTOR
 - BTH_LE_GATT_DESCRIPTOR
 - bthledef/BTH_LE_GATT_DESCRIPTOR
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
 - BTH_LE_GATT_DESCRIPTOR
---

# BTH_LE_GATT_DESCRIPTOR structure


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

<a href="/windows/desktop/api/bthledef/ne-bthledef-bth_le_gatt_descriptor_type">BTH_LE_GATT_DESCRIPTOR_TYPE</a>



<a href="/windows/desktop/api/bthledef/ns-bthledef-bth_le_uuid">BTH_LE_UUID</a>



<a href="/windows/desktop/api/bluetoothleapis/nf-bluetoothleapis-bluetoothgattgetdescriptorvalue">BluetoothGATTGetDescriptorValue</a>



<a href="/windows/desktop/api/bluetoothleapis/nf-bluetoothleapis-bluetoothgattgetdescriptors">BluetoothGATTGetDescriptors</a>



<a href="/windows/desktop/api/bluetoothleapis/nf-bluetoothleapis-bluetoothgattsetdescriptorvalue">BluetoothGATTSetDescriptorValue</a>