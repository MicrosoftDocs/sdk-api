---
UID: NS:bthledef._BLUETOOTH_GATT_VALUE_CHANGED_EVENT
title: BLUETOOTH_GATT_VALUE_CHANGED_EVENT (bthledef.h)
author: windows-sdk-content
description: The BLUETOOTH_GATT_VALUE_CHANGED_EVENT structure describes a changed attribute value.
old-location: bltooth\bluetooth_gatt_value_changed_event.htm
tech.root: bltooth
ms.assetid: EC6E5B85-495E-401B-ADE5-D51891A4BDFE
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PBLUETOOTH_GATT_VALUE_CHANGED_EVENT, BLUETOOTH_GATT_VALUE_CHANGED_EVENT, BLUETOOTH_GATT_VALUE_CHANGED_EVENT structure [Bluetooth Devices], PBLUETOOTH_GATT_VALUE_CHANGED_EVENT, PBLUETOOTH_GATT_VALUE_CHANGED_EVENT structure pointer [Bluetooth Devices], bltooth.bluetooth_gatt_value_changed_event, bthledef/BLUETOOTH_GATT_VALUE_CHANGED_EVENT, bthledef/PBLUETOOTH_GATT_VALUE_CHANGED_EVENT"
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
 - BLUETOOTH_GATT_VALUE_CHANGED_EVENT
product: Windows
targetos: Windows
req.typenames: BLUETOOTH_GATT_VALUE_CHANGED_EVENT, *PBLUETOOTH_GATT_VALUE_CHANGED_EVENT
req.redist: 
---

# BLUETOOTH_GATT_VALUE_CHANGED_EVENT structure


## -description


The BLUETOOTH_GATT_VALUE_CHANGED_EVENT structure describes a changed attribute value.


## -struct-fields




### -field ChangedAttributeHandle

The handle to the attribute.


### -field CharacteristicValueDataSize

The size, in bytes, of <b>CharacteristicValue</b>.


### -field CharacteristicValue

The characteristic value.


## -see-also




<a href="https://msdn.microsoft.com/AF36BC9A-5EB7-4495-870A-40BF5E0A57A3">BTH_LE_GATT_CHARACTERISTIC_VALUE</a>
 

 

