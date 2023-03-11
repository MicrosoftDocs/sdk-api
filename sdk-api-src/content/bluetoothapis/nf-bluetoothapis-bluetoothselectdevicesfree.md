---
UID: NF:bluetoothapis.BluetoothSelectDevicesFree
title: BluetoothSelectDevicesFree function (bluetoothapis.h)
description: Frees resources associated with a previous call to BluetoothSelectDevices.
helpviewer_keywords: ["BluetoothSelectDevicesFree","BluetoothSelectDevicesFree function [Bluetooth]","_bth_bluetoothselectdevicesfree","bluetooth.bluetoothselectdevicesfree","bluetoothapis/BluetoothSelectDevicesFree"]
old-location: bluetooth\bluetoothselectdevicesfree.htm
tech.root: bluetooth
ms.assetid: 9332e62d-a7ee-452e-8e21-27bbbc82448e
ms.date: 12/05/2018
ms.keywords: BluetoothSelectDevicesFree, BluetoothSelectDevicesFree function [Bluetooth], _bth_bluetoothselectdevicesfree, bluetooth.bluetoothselectdevicesfree, bluetoothapis/BluetoothSelectDevicesFree
req.header: bluetoothapis.h
req.include-header: Bthsdpdef.h, BluetoothAPIs.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bthprops.lib
req.dll: bthprops.cpl
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BluetoothSelectDevicesFree
 - bluetoothapis/BluetoothSelectDevicesFree
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - bthprops.cpl
api_name:
 - BluetoothSelectDevicesFree
---

# BluetoothSelectDevicesFree function


## -description

The 
<b>BluetoothSelectDevicesFree</b> function frees resources associated with a previous call to 
<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothselectdevices">BluetoothSelectDevices</a>.

## -parameters

### -param pbtsdp

A pointer to a 
<a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_select_device_params">BLUETOOTH_SELECT_DEVICE_PARAMS</a> structure that identifies the Bluetooth device resources to free.

## -returns

Returns <b>TRUE</b> upon success. Returns <b>FALSE</b> if there are no resources to free.

## -remarks

Only call the <b>BluetoothSelectDevicesFree</b> function if a previous call to the <a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothselectdevices">BluetoothSelectDevices</a> function returned <b>TRUE</b>.

## -see-also

<a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_select_device_params">BLUETOOTH_SELECT_DEVICE_PARAMS</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothselectdevices">BluetoothSelectDevices</a>