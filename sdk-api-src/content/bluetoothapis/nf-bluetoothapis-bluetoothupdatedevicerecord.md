---
UID: NF:bluetoothapis.BluetoothUpdateDeviceRecord
title: BluetoothUpdateDeviceRecord function (bluetoothapis.h)
description: Updates the local computer cache about a Bluetooth device.
helpviewer_keywords: ["BluetoothUpdateDeviceRecord","BluetoothUpdateDeviceRecord function [Bluetooth]","bluetooth.bluetoothupdatedevicerecord","bluetoothapis/BluetoothUpdateDeviceRecord"]
old-location: bluetooth\bluetoothupdatedevicerecord.htm
tech.root: bluetooth
ms.assetid: afcf6708-1c2a-43ac-8e5e-1bd0ce7456fc
ms.date: 12/05/2018
ms.keywords: BluetoothUpdateDeviceRecord, BluetoothUpdateDeviceRecord function [Bluetooth], bluetooth.bluetoothupdatedevicerecord, bluetoothapis/BluetoothUpdateDeviceRecord
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
 - BluetoothUpdateDeviceRecord
 - bluetoothapis/BluetoothUpdateDeviceRecord
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
 - BluetoothUpdateDeviceRecord
---

# BluetoothUpdateDeviceRecord function


## -description

The <b>BluetoothUpdateDeviceRecord</b> function updates the local computer cache about a Bluetooth device.

## -parameters

### -param pbtdi

A pointer to the <a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_info_struct">BLUETOOTH_DEVICE_INFO</a> structure to update. For more information, see the Remarks section.

## -returns

Returns <b>ERROR_SUCCESS</b> upon success. The following table  lists common errors.

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
The <i>pbtdi</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_REVISION_MISMATCH</b></dt>
</dl>
</td>
<td width="60%">
The <b>dwSize</b> member of the structure pointed to in the <i>pbtdi</i> parameter is not valid.

</td>
</tr>
</table>

## -remarks

When updating a Bluetooth device record, the requirements for members of the <a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_info_struct">BLUETOOTH_DEVICE_INFO</a> structure, listed in the following table, must be observed.<table>
<tr>
<th>Member</th>
<th>Requirement</th>
</tr>
<tr>
<td><b>dwSize</b></td>
<td>Must match the structure size.</td>
</tr>
<tr>
<td><b>Address</b></td>
<td>Must be a previously found radio address.</td>
</tr>
<tr>
<td><b>szName</b></td>
<td>Must contain the new name to be stored.</td>
</tr>
</table>

## -see-also

<a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_info_struct">BLUETOOTH_DEVICE_INFO</a>



<a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_search_params">BLUETOOTH_DEVICE_SEARCH_PARAMS</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothdisplaydeviceproperties">BluetoothDisplayDeviceProperties</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothfinddeviceclose">BluetoothFindDeviceClose</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothfindfirstdevice">BluetoothFindFirstDevice</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothfindnextdevice">BluetoothFindNextDevice</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothgetdeviceinfo">BluetoothGetDeviceInfo</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothremovedevice">BluetoothRemoveDevice</a>