---
UID: NF:bluetoothapis.BluetoothDisplayDeviceProperties
title: BluetoothDisplayDeviceProperties function (bluetoothapis.h)
description: Starts Control Panel device information property sheet.
helpviewer_keywords: ["BluetoothDisplayDeviceProperties","BluetoothDisplayDeviceProperties function [Bluetooth]","bluetooth.bluetoothdisplaydeviceproperties","bluetoothapis/BluetoothDisplayDeviceProperties"]
old-location: bluetooth\bluetoothdisplaydeviceproperties.htm
tech.root: bluetooth
ms.assetid: cb33cf35-eb1e-4953-a779-4eb38afe0c34
ms.date: 12/05/2018
ms.keywords: BluetoothDisplayDeviceProperties, BluetoothDisplayDeviceProperties function [Bluetooth], bluetooth.bluetoothdisplaydeviceproperties, bluetoothapis/BluetoothDisplayDeviceProperties
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
 - BluetoothDisplayDeviceProperties
 - bluetoothapis/BluetoothDisplayDeviceProperties
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
 - BluetoothDisplayDeviceProperties
---

# BluetoothDisplayDeviceProperties function


## -description

The <b>BluetoothDisplayDeviceProperties</b> function starts Control Panel device information property sheet.

## -parameters

### -param hwndParent

A handle to the parent window of the property sheet.

### -param pbtdi

A pointer to the <a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_info_struct">BLUETOOTH_DEVICE_INFO</a> structure that contains information about the Bluetooth device.

## -returns

Returns <b>TRUE</b> if the property sheet is successfully displayed. Returns <b>FALSE</b> if the property sheet was not displayed successfully; call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function for additional error information.

## -see-also

<a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_info_struct">BLUETOOTH_DEVICE_INFO</a>



<a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_search_params">BLUETOOTH_DEVICE_SEARCH_PARAMS</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothfinddeviceclose">BluetoothFindDeviceClose</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothfindfirstdevice">BluetoothFindFirstDevice</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothfindnextdevice">BluetoothFindNextDevice</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothgetdeviceinfo">BluetoothGetDeviceInfo</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothremovedevice">BluetoothRemoveDevice</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothupdatedevicerecord">BluetoothUpdateDeviceRecord</a>