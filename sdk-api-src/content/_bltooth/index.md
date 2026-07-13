---
UID: TP:bltooth
title: Bluetooth devices reference
ms.assetid: a24d2124-fb4a-3c14-aeb8-83c46e9ed71c
ms.date: 10/20/2022
ms.keywords: 
ms.topic: overview
ms.update-cycle: 1095-days
---

# Bluetooth devices reference

## -description

Overview of the Bluetooth devices reference technology.

To develop Bluetooth devices reference, you need these headers:

 * [bluetoothleapis.h](../bluetoothleapis/index.md)
 * [bthledef.h](../bthledef/index.md)

For programming guidance for this technology, see:
* [Bluetooth Devices Reference](/windows-hardware/drivers/bluetooth/)

## GUIDs

The following GUIDs are defined in the `bthledef.h` header file. To enumerate paired Bluetooth LE devices, you can use the [SetupDiXxx](/windows/win32/api/setupapi/) Win32 enumeration APIs to enumerate devices of the **GUID_BLUETOOTHLE_DEVICE_INTERFACE** device interface class.

|GUID name, description|Value|
|-|-|
|**GUID_BLUETOOTHLE_DEVICE_INTERFACE**. Bluetooth LE device interface GUID. |0x781aee18, 0x7733, 0x4ce4, 0xad, 0xd0, 0x91, 0xf4, 0x1c, 0x67, 0xb5, 0x92|
|**GUID_BLUETOOTH_GATT_SERVICE_DEVICE_INTERFACE**. Bluetooth LE Service device interface GUID. |0x6e3bb679, 0x4372, 0x40c8, 0x9e, 0xaa, 0x45, 0x09, 0xdf, 0x26, 0x0c, 0xd8|
|**BTH_LE_ATT_BLUETOOTH_BASE_GUID**. Bluetooth base GUID. |0x00000000, 0x0000, 0x1000, 0x80, 0x00, 0x00, 0x80, 0x5F, 0x9B, 0x34, 0xFB|
