---
UID: NF:bluetoothapis.BluetoothFindFirstDevice
title: BluetoothFindFirstDevice function (bluetoothapis.h)
description: The BluetoothFindFirstDevice function begins the enumeration Bluetooth devices.
helpviewer_keywords: ["BluetoothFindFirstDevice","BluetoothFindFirstDevice function [Bluetooth]","bluetooth.bluetoothfindfirstdevice","bluetoothapis/BluetoothFindFirstDevice"]
old-location: bluetooth\bluetoothfindfirstdevice.htm
tech.root: bluetooth
ms.assetid: f73acbb4-119f-4a73-a338-d11e8cf7e6be
ms.date: 12/05/2018
ms.keywords: BluetoothFindFirstDevice, BluetoothFindFirstDevice function [Bluetooth], bluetooth.bluetoothfindfirstdevice, bluetoothapis/BluetoothFindFirstDevice
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
 - BluetoothFindFirstDevice
 - bluetoothapis/BluetoothFindFirstDevice
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
 - BluetoothFindFirstDevice
---

# BluetoothFindFirstDevice function


## -description

The <b>BluetoothFindFirstDevice</b> function begins the enumeration Bluetooth devices.

## -parameters

### -param pbtsp

Pointer to a <a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_search_params">BLUETOOTH_DEVICE_SEARCH_PARAMS</a> structure. The <b>dwSize</b> member of the <b>BLUETOOTH_DEVICE_SEARCH_PARAMS</b> structure pointed to by <i>pbtsp</i> must match the size of the structure.

### -param pbtdi

Pointer to a <a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_info_struct">BLUETOOTH_DEVICE_INFO</a> structure into which information about the first Bluetooth device found is placed. The <b>dwSize</b> member of the <b>BLUETOOTH_DEVICE_INFO</b> structure pointed to by <i>pbtdi</i> must match the size of the structure, or the call to the <b>BluetoothFindFirstDevice</b> function fails.

## -returns

Returns a valid handle to the first Bluetooth device upon successful completion, and the <i>pbtdi</i> parameter points to information about the device. When this handle is no longer needed, it must be closed via the <a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothfinddeviceclose">BluetoothFindDeviceClose</a>.

Returns <b>NULL</b> upon failure. Call the  <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function for more information on the error. The following table  describe common errors:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pbtsp</i> or <i>pbtdi</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_REVISION_MISMATCH</b></dt>
</dl>
</td>
<td width="60%">
The structure pointed to by <i>pbtsp</i> or <i>pbtdi</i> is not the correct size.

</td>
</tr>
</table>

## -remarks

The BluetoothFindFirstDevice function does not find Bluetooth Low Energy (LE) devices.
To access Bluetooth LE devices, use the
<a href="/windows/uwp/devices-sensors/bluetooth-low-energy-overview">Windows Runtime Bluetooth Low Energy APIs</a>.
The Windows Runtime APIs for Bluetooth work in both UWP and classic desktop apps.

## -see-also

<a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_info_struct">BLUETOOTH_DEVICE_INFO</a>



<a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_search_params">BLUETOOTH_DEVICE_SEARCH_PARAMS</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothdisplaydeviceproperties">BluetoothDisplayDeviceProperties</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothfinddeviceclose">BluetoothFindDeviceClose</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothfindnextdevice">BluetoothFindNextDevice</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothgetdeviceinfo">BluetoothGetDeviceInfo</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothremovedevice">BluetoothRemoveDevice</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothupdatedevicerecord">BluetoothUpdateDeviceRecord</a>