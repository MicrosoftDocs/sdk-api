---
UID: NC:bluetoothapis.PFN_DEVICE_CALLBACK
title: PFN_DEVICE_CALLBACK (bluetoothapis.h)
description: A callback prototype used in association with selecting Bluetooth devices.
helpviewer_keywords: ["PFN_DEVICE_CALLBACK","PFN_DEVICE_CALLBACK callback","PFN_DEVICE_CALLBACK callback function [Bluetooth]","bluetooth.pfn_device_callback","bluetoothapis/PFN_DEVICE_CALLBACK"]
old-location: bluetooth\pfn_device_callback.htm
tech.root: bluetooth
ms.assetid: 8a2bf4dc-43c3-49c0-8ce0-d14ab9f4ae97
ms.date: 12/05/2018
ms.keywords: PFN_DEVICE_CALLBACK, PFN_DEVICE_CALLBACK callback, PFN_DEVICE_CALLBACK callback function [Bluetooth], bluetooth.pfn_device_callback, bluetoothapis/PFN_DEVICE_CALLBACK
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PFN_DEVICE_CALLBACK
 - bluetoothapis/PFN_DEVICE_CALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - BluetoothAPIs.h
api_name:
 - PFN_DEVICE_CALLBACK
---

# PFN_DEVICE_CALLBACK callback function


## -description

The <b>PFN_DEVICE_CALLBACK</b> function is a callback prototype used in association with selecting Bluetooth devices. The 
<b>PFN_DEVICE_CALLBACK</b> function can be set to <b>NULL</b> if no specialized filtering is required.

## -parameters

### -param pvParam

A parameter passed in from  the <b>pvParam</b> member of the 
<a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_select_device_params">BLUETOOTH_SELECT_DEVICE_PARAMS</a> structure through the <a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothselectdevices">BluetoothSelectDevices</a> function.

### -param pDevice

Remote Bluetooth address queried; this is the address inserted into the user-presented list of Bluetooth devices.

## -returns

Returning <b>FALSE</b> prevents the device from being added to the list view of Bluetooth devices.

## -remarks

The 
<a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_info_struct">BLUETOOTH_DEVICE_INFO</a> structure pointed to in <i>pDevice</i> is the device that the 
<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothselectdevices">BluetoothSelectDevices</a> function is querying to determine if that device should be added to the list view.

If the callback performs SDP queries for each device, the list of devices from which the user can choose will be delayed until all devices can be queried. A recommended approach is to use the service to call bitfield in the class of device, available through <b>GET_COD_SERVICE</b>, to determine whether the device should be displayed to the user. The service class bitfield is available in the <b>pDevice</b> parameter through the <b>ulClassOfDevice</b> member.

## -see-also

<a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_info_struct">BLUETOOTH_DEVICE_INFO</a>



<a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_select_device_params">BLUETOOTH_SELECT_DEVICE_PARAMS</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothselectdevices">BluetoothSelectDevices</a>
