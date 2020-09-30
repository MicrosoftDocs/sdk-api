---
UID: NS:bthledef._BLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION
title: BLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION (bthledef.h)
description: The BLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION structure describes one or more characteristics that have changed.
helpviewer_keywords: ["*PBLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION","BLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION","BLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION structure [Bluetooth Devices]","PBLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION","PBLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION structure pointer [Bluetooth Devices]","bltooth.bluetooth_gatt_value_changed_event_registration","bthledef/BLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION","bthledef/PBLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION"]
old-location: bltooth\bluetooth_gatt_value_changed_event_registration.htm
tech.root: bltooth
ms.assetid: 97EB32A7-87BF-4DBA-9480-4BB7DFCBFB23
ms.date: 12/05/2018
ms.keywords: '*PBLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION, BLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION, BLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION structure [Bluetooth Devices], PBLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION, PBLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION structure pointer [Bluetooth Devices], bltooth.bluetooth_gatt_value_changed_event_registration, bthledef/BLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION, bthledef/PBLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION'
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
req.typenames: BLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION, *PBLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _BLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION
 - bthledef/_BLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION
 - PBLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION
 - bthledef/PBLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION
 - BLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION
 - bthledef/BLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION
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
 - BLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION
---

## -description

The BLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION structure describes one or more characteristics that have changed.

## -struct-fields

### -field NumCharacteristics

The number of characteristics that follow this member in memory.

### -field Characteristics

Array of characteristics to monitor for incoming events.

## -see-also

<a href="/windows/win32/api/bthledef/ns-bthledef-bth_le_gatt_characteristic">BTH_LE_GATT_CHARACTERISTIC</a>

