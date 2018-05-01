---
UID: NS:bthledef._BLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION
title: "_BLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION"
author: windows-driver-content
description: The BLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION structure describes one or more characteristics that have changed.
old-location: bltooth\bluetooth_gatt_value_changed_event_registration.htm
old-project: bltooth
ms.assetid: 97EB32A7-87BF-4DBA-9480-4BB7DFCBFB23
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: "*PBLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION, BLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION, BLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION structure [Bluetooth Devices], PBLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION, PBLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION structure pointer [Bluetooth Devices], _BLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION, bltooth.bluetooth_gatt_value_changed_event_registration, bthledef/BLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION, bthledef/PBLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION"
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
req.typenames: BLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION, *PBLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	BthLEDef.h
api_name:
-	BLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _BLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION structure


## -description


The BLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION structure describes one or more characteristics that have changed.


## -struct-fields




### -field NumCharacteristics

The number of characteristics that follow this member in memory.


### -field Characteristics

 




#### - Characteristics[1]

Array of characteristics to monitor for incoming events.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/hh450840">BTH_LE_GATT_CHARACTERISTIC</a>
 

 

