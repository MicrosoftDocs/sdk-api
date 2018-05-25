---
UID: TP:bltooth
ms.assetid: a24d2124-fb4a-3c14-aeb8-83c46e9ed71c
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
---

# Bluetooth Devices Reference



Overview of the Bluetooth Devices Reference technology.

To develop Bluetooth Devices Reference, you need these headers:

 * [bluetoothleapis.h](..\bluetoothleapis\index.md)
 * [bthledef.h](..\bthledef\index.md)

For the programming guide, see [Bluetooth Devices Reference](/windows/desktop/bltooth).

## Functions

| Title   | Description   |
| ---- |:---- |
| [BluetoothGATTAbortReliableWrite function](..\bluetoothleapis\nf-bluetoothleapis-bluetoothgattabortreliablewrite.md) | Specifies the end of reliable write procedures, and the writes should be aborted. |
| [BluetoothGATTBeginReliableWrite function](..\bluetoothleapis\nf-bluetoothleapis-bluetoothgattbeginreliablewrite.md) | The BluetoothGATTBeginReliableWrite function specifies that reliable writes are about to begin. |
| [BluetoothGATTEndReliableWrite function](..\bluetoothleapis\nf-bluetoothleapis-bluetoothgattendreliablewrite.md) | Specifies the end of reliable writes, and the writes should be committed. |
| [BluetoothGATTGetCharacteristicValue function](..\bluetoothleapis\nf-bluetoothleapis-bluetoothgattgetcharacteristicvalue.md) | Gets the value of the specified characteristic. |
| [BluetoothGATTGetCharacteristics function](..\bluetoothleapis\nf-bluetoothleapis-bluetoothgattgetcharacteristics.md) | Gets all the characteristics available for the specified service. |
| [BluetoothGATTGetDescriptorValue function](..\bluetoothleapis\nf-bluetoothleapis-bluetoothgattgetdescriptorvalue.md) | Gets the value of the specified descriptor. |
| [BluetoothGATTGetDescriptors function](..\bluetoothleapis\nf-bluetoothleapis-bluetoothgattgetdescriptors.md) | Gets all the descriptors available for the specified characteristic. |
| [BluetoothGATTGetIncludedServices function](..\bluetoothleapis\nf-bluetoothleapis-bluetoothgattgetincludedservices.md) | Gets all the included services available for a given service. |
| [BluetoothGATTGetServices function](..\bluetoothleapis\nf-bluetoothleapis-bluetoothgattgetservices.md) | The BluetoothGATTGetServices function gets all the primary services available for a server. |
| [BluetoothGATTRegisterEvent function](..\bluetoothleapis\nf-bluetoothleapis-bluetoothgattregisterevent.md) | Registers a routine to be called back during a characteristic value change event on the given characteristic identified by its characteristic handle. |
| [BluetoothGATTSetCharacteristicValue function](..\bluetoothleapis\nf-bluetoothleapis-bluetoothgattsetcharacteristicvalue.md) | Writes the specified characteristic value to the Bluetooth device. |
| [BluetoothGATTSetDescriptorValue function](..\bluetoothleapis\nf-bluetoothleapis-bluetoothgattsetdescriptorvalue.md) | Writes the specified descriptor value to the Bluetooth device. |
| [BluetoothGATTUnregisterEvent function](..\bluetoothleapis\nf-bluetoothleapis-bluetoothgattunregisterevent.md) | Unregisters the given characteristic value change event. |

## Callback functions

| Title   | Description   |
| ---- |:---- |
| [PFNBLUETOOTH_GATT_EVENT_CALLBACK callback function](..\bthledef\nc-bthledef-pfnbluetooth_gatt_event_callback.md) | Profile drivers implement a Bluetooth GATT event callback to be called whenever the value of a specific characteristic changes. |

## Structures

| Title   | Description   |
| ---- |:---- |
| [_BLUETOOTH_GATT_VALUE_CHANGED_EVENT structure](..\bthledef\ns-bthledef-_bluetooth_gatt_value_changed_event.md) | The BLUETOOTH_GATT_VALUE_CHANGED_EVENT structure describes a changed attribute value. |
| [_BLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION structure](..\bthledef\ns-bthledef-_bluetooth_gatt_value_changed_event_registration.md) | The BLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION structure describes one or more characteristics that have changed. |
| [_BTH_LE_GATT_CHARACTERISTIC structure](..\bthledef\ns-bthledef-_bth_le_gatt_characteristic.md) | The BTH_LE_GATT_CHARACTERISTIC structure describes a Bluetooth Low Energy (LE) generic attribute (GATT) profile characteristic. |
| [_BTH_LE_GATT_CHARACTERISTIC_VALUE structure](..\bthledef\ns-bthledef-_bth_le_gatt_characteristic_value.md) | The BTH_LE_GATT_CHARACTERISTIC_VALUE structure describes a Bluetooth Low Energy (LE) generic attribute (GATT) profile characteristic value. |
| [_BTH_LE_GATT_DESCRIPTOR structure](..\bthledef\ns-bthledef-_bth_le_gatt_descriptor.md) | The BTH_LE_GATT_DESCRIPTOR structure describes a Bluetooth Low Energy (LE) generic attribute (GATT) profile descriptor. |
| [_BTH_LE_GATT_DESCRIPTOR_VALUE structure](..\bthledef\ns-bthledef-_bth_le_gatt_descriptor_value.md) | The BTH_LE_GATT_DESCRIPTOR_VALUE structure describes a parent characteristic. |
| [_BTH_LE_GATT_SERVICE structure](..\bthledef\ns-bthledef-_bth_le_gatt_service.md) | The BTH_LE_GATT_SERVICE structure describes a Bluetooth Low Energy (LE) generic attribute (GATT) profile service. |
| [_BTH_LE_UUID structure](..\bthledef\ns-bthledef-_bth_le_uuid.md) | The BTH_LE_UUID structure contains information about a Bluetooth Low Energy (LE) Universally Unique Identifier (UUID). |

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [_BTH_LE_GATT_DESCRIPTOR_TYPE enumeration](..\bthledef\ne-bthledef-_bth_le_gatt_descriptor_type.md) | The BTH_LE_GATT_DESCRIPTOR_TYPE enumeration describes the different types of Bluetooth LE generic attributes (GATT). |
| [_BTH_LE_GATT_EVENT_TYPE enumeration](..\bthledef\ne-bthledef-_bth_le_gatt_event_type.md) | The BTH_LE_GATT_EVENT_TYPE enumeration describes the different types of Bluetooth Low Energy (LE) generic attribute (GATT) profile events. |
