---
UID: NF:bluetoothapis.BluetoothRemoveDevice
title: BluetoothRemoveDevice function (bluetoothapis.h)
description: Removes authentication between a Bluetooth device and the computer and clears cached service information for the device.
helpviewer_keywords: ["BluetoothRemoveDevice","BluetoothRemoveDevice function [Bluetooth]","bluetooth.bluetoothremovedevice","bluetoothapis/BluetoothRemoveDevice"]
old-location: bluetooth\bluetoothremovedevice.htm
tech.root: bluetooth
ms.assetid: dd4f6468-ccc2-4072-95c5-97553308ae47
ms.date: 12/05/2018
ms.keywords: BluetoothRemoveDevice, BluetoothRemoveDevice function [Bluetooth], bluetooth.bluetoothremovedevice, bluetoothapis/BluetoothRemoveDevice
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
 - BluetoothRemoveDevice
 - bluetoothapis/BluetoothRemoveDevice
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - bthprops.cpl
 - BluetoothAPIs.dll
 - Ext-MS-Win-Bluetooth-APIs-l1-1-0.dll
api_name:
 - BluetoothRemoveDevice
---

# BluetoothRemoveDevice function


## -description

The <b>BluetoothRemoveDevice</b> function removes authentication between a Bluetooth device and the computer and clears cached service information for the device.

## -parameters

### -param pAddress

A pointer to the address of the Bluetooth device to be removed.

## -returns

Returns <b>ERROR_SUCCESS</b> upon successful removal of the Bluetooth device. Returns <b>ERROR_NOT_FOUND</b> if the device was not found.

## -remarks

The <b>BluetoothRemoveDevice</b> function fails if the device indicated by <i>pAddress</i> is not a remembered device.

## -see-also

<a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_info_struct">BLUETOOTH_DEVICE_INFO</a>



<a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_search_params">BLUETOOTH_DEVICE_SEARCH_PARAMS</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothdisplaydeviceproperties">BluetoothDisplayDeviceProperties</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothfinddeviceclose">BluetoothFindDeviceClose</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothfindfirstdevice">BluetoothFindFirstDevice</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothfindnextdevice">BluetoothFindNextDevice</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothgetdeviceinfo">BluetoothGetDeviceInfo</a>