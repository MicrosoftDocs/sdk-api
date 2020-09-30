---
UID: NS:bthledef._BTH_LE_GATT_SERVICE
title: BTH_LE_GATT_SERVICE (bthledef.h)
description: The BTH_LE_GATT_SERVICE structure describes a Bluetooth Low Energy (LE) generic attribute (GATT) profile service.
helpviewer_keywords: ["*PBTH_LE_GATT_SERVICE","BTH_LE_GATT_SERVICE","BTH_LE_GATT_SERVICE structure [Bluetooth Devices]","PBTH_LE_GATT_SERVICE","PBTH_LE_GATT_SERVICE structure pointer [Bluetooth Devices]","bltooth.bth_le_gatt_service","bthledef/BTH_LE_GATT_SERVICE","bthledef/PBTH_LE_GATT_SERVICE"]
old-location: bltooth\bth_le_gatt_service.htm
tech.root: bltooth
ms.assetid: B4433D0F-7938-4C6D-994F-D99393EC013A
ms.date: 12/05/2018
ms.keywords: '*PBTH_LE_GATT_SERVICE, BTH_LE_GATT_SERVICE, BTH_LE_GATT_SERVICE structure [Bluetooth Devices], PBTH_LE_GATT_SERVICE, PBTH_LE_GATT_SERVICE structure pointer [Bluetooth Devices], bltooth.bth_le_gatt_service, bthledef/BTH_LE_GATT_SERVICE, bthledef/PBTH_LE_GATT_SERVICE'
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
req.typenames: BTH_LE_GATT_SERVICE, *PBTH_LE_GATT_SERVICE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _BTH_LE_GATT_SERVICE
 - bthledef/_BTH_LE_GATT_SERVICE
 - PBTH_LE_GATT_SERVICE
 - bthledef/PBTH_LE_GATT_SERVICE
 - BTH_LE_GATT_SERVICE
 - bthledef/BTH_LE_GATT_SERVICE
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
 - BTH_LE_GATT_SERVICE
---

# BTH_LE_GATT_SERVICE structure


## -description

The BTH_LE_GATT_SERVICE structure describes a Bluetooth Low Energy (LE) generic attribute (GATT) profile service.

## -struct-fields

### -field ServiceUuid

The Universally Unique ID (UUID) of the Bluetooth LE GATT profile service.

### -field AttributeHandle

The handle to the Bluetooth LE GATT profile attributes.

## -see-also

<a href="/windows/desktop/api/bthledef/ns-bthledef-bth_le_uuid">BTH_LE_UUID</a>



<a href="/windows/desktop/api/bluetoothleapis/nf-bluetoothleapis-bluetoothgattgetcharacteristics">BluetoothGATTGetCharacteristics</a>



<a href="/windows/desktop/api/bluetoothleapis/nf-bluetoothleapis-bluetoothgattgetincludedservices">BluetoothGATTGetIncludedServices</a>



<a href="/windows/desktop/api/bluetoothleapis/nf-bluetoothleapis-bluetoothgattgetservices">BluetoothGATTGetServices</a>