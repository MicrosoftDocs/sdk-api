---
UID: NC:bthledef.PFNBLUETOOTH_GATT_EVENT_CALLBACK
title: PFNBLUETOOTH_GATT_EVENT_CALLBACK (bthledef.h)
description: Profile drivers implement a Bluetooth GATT event callback to be called whenever the value of a specific characteristic changes.
helpviewer_keywords: ["BluetoothGattEventCallback","BluetoothGattEventCallback callback function [Bluetooth Devices]","PFNBLUETOOTH_GATT_EVENT_CALLBACK","PFNBLUETOOTH_GATT_EVENT_CALLBACK callback","bltooth.bluetooth_gatt_notification_callback_function","bthledef/BluetoothGattEventCallback"]
old-location: bltooth\bluetooth_gatt_notification_callback_function.htm
tech.root: bltooth
ms.assetid: 96AC4E49-76D7-47B5-93B9-64D574A28E0A
ms.date: 12/05/2018
ms.keywords: BluetoothGattEventCallback, BluetoothGattEventCallback callback function [Bluetooth Devices], PFNBLUETOOTH_GATT_EVENT_CALLBACK, PFNBLUETOOTH_GATT_EVENT_CALLBACK callback, bltooth.bluetooth_gatt_notification_callback_function, bthledef/BluetoothGattEventCallback
req.header: bthledef.h
req.include-header: 
req.target-type: Desktop
req.target-min-winverclnt: Supported in Windows 8 and later versions of Windows.
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PFNBLUETOOTH_GATT_EVENT_CALLBACK
 - bthledef/PFNBLUETOOTH_GATT_EVENT_CALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - bthledef.h
api_name:
 - BluetoothGattEventCallback
---

# PFNBLUETOOTH_GATT_EVENT_CALLBACK callback function


## -description

Profile drivers implement a Bluetooth GATT event callback to be called whenever the value of a specific characteristic changes.

## -parameters

### -param EventType [in]

The type of GATT event.

### -param EventOutParameter [in]

Pointer to a <a href="/windows/win32/api/bthledef/ns-bthledef-bluetooth_gatt_value_changed_event">BLUETOOTH_GATT_VALUE_CHANGED_EVENT</a> structure.

### -param Context [in, optional]

The context specified by the profile driver in the <i>CallbackContext</i> parameter of 
      the <a href="/windows/desktop/api/bluetoothleapis/nf-bluetoothleapis-bluetoothgattregisterevent">BluetoothGATTRegisterEvent</a> function 
      when the profile driver registered the GATT callback function.

## -see-also

<a href="/windows/win32/api/bthledef/ns-bthledef-bluetooth_gatt_value_changed_event">BLUETOOTH_GATT_VALUE_CHANGED_EVENT</a>



<a href="/windows/desktop/api/bthledef/ne-bthledef-bth_le_gatt_event_type">BTH_LE_GATT_EVENT_TYPE</a>



<a href="/windows/desktop/api/bluetoothleapis/nf-bluetoothleapis-bluetoothgattregisterevent">BluetoothGATTRegisterEvent</a>