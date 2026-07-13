---
UID: NF:bluetoothapis.BluetoothSelectDevices
title: BluetoothSelectDevices function (bluetoothapis.h)
description: Enables Bluetooth device selection.
helpviewer_keywords: ["BluetoothSelectDevices","BluetoothSelectDevices function [Bluetooth]","_bth_bluetoothselectdevices","bluetooth.bluetoothselectdevices","bluetoothapis/BluetoothSelectDevices"]
old-location: bluetooth\bluetoothselectdevices.htm
tech.root: bluetooth
ms.assetid: 97fcbd72-99d5-4c5b-bf16-75eea97cbc77
ms.date: 12/05/2018
ms.keywords: BluetoothSelectDevices, BluetoothSelectDevices function [Bluetooth], _bth_bluetoothselectdevices, bluetooth.bluetoothselectdevices, bluetoothapis/BluetoothSelectDevices
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
 - BluetoothSelectDevices
 - bluetoothapis/BluetoothSelectDevices
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
 - BluetoothSelectDevices
---

# BluetoothSelectDevices function


## -description

The 
<b>BluetoothSelectDevices</b> function enables Bluetooth device selection.

## -parameters

### -param pbtsdp

A pointer to a 
<a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_select_device_params">BLUETOOTH_SELECT_DEVICE_PARAMS</a> structure that identifies Bluetooth devices.

## -returns

Returns <b>TRUE</b> if a user selected a device.

Returns <b>FALSE</b> if no valid data was returned. Call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function to retrieve error information. The following conditions apply to returned error information.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
The user canceled the request.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pbtsdp</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_REVISION_MISMATCH</b></dt>
</dl>
</td>
<td width="60%">
The structure passed in <i>pbtsdp</i> is of unknown size.

</td>
</tr>
</table>

## -remarks

The <b>BluetoothSelectDevices</b> function opens a common dialog box for selecting Bluetooth devices. The list of devices displayed to the user is determined by the flags and settings the caller specifies in the <i>pbtsdp</i> parameter.

If 
<b>BluetoothSelectDevices</b> returns <b>TRUE</b>, the <b>pDevices</b> member of the 
<a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_select_device_params">BLUETOOTH_SELECT_DEVICE_PARAMS</a> structure points to valid data. The caller should verify that  the <b>fAuthenticated</b> and <b>fRemembered</b> flags in the 
<b>BLUETOOTH_SELECT_DEVICE_PARAMS</b> structure to determine which devices were successfully authenticated, and which devices are valid selections for the user. Call the 
<b>BluetoothSelectDevicesFree</b> function to free resources only if the 
<b>BluetoothSelectDevices</b> function returns <b>TRUE</b>.

## -see-also

<a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_select_device_params">BLUETOOTH_SELECT_DEVICE_PARAMS</a>



<a href="/windows/desktop/api/bluetoothapis/nc-bluetoothapis-pfn_device_callback">PFN_DEVICE_CALLBACK</a>