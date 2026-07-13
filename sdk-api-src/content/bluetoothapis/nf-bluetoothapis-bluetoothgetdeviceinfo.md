---
UID: NF:bluetoothapis.BluetoothGetDeviceInfo
title: BluetoothGetDeviceInfo function (bluetoothapis.h)
description: Retrieves information about a remote Bluetooth device.
helpviewer_keywords: ["BluetoothGetDeviceInfo","BluetoothGetDeviceInfo function [Bluetooth]","bluetooth.bluetoothgetdeviceinfo","bluetoothapis/BluetoothGetDeviceInfo"]
old-location: bluetooth\bluetoothgetdeviceinfo.htm
tech.root: bluetooth
ms.assetid: 530e5131-a0ab-4ddd-be73-a07f94e74f73
ms.date: 12/05/2018
ms.keywords: BluetoothGetDeviceInfo, BluetoothGetDeviceInfo function [Bluetooth], bluetooth.bluetoothgetdeviceinfo, bluetoothapis/BluetoothGetDeviceInfo
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
 - BluetoothGetDeviceInfo
 - bluetoothapis/BluetoothGetDeviceInfo
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
 - BluetoothGetDeviceInfo
---

# BluetoothGetDeviceInfo function


## -description

The <b>BluetoothGetDeviceInfo</b> function retrieves information about a remote Bluetooth device. The Bluetooth device must have been previously identified through a successful device inquiry function call.

## -parameters

### -param hRadio

A handle to a local radio, obtained from a call to the <a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothfindfirstradio">BluetoothFindFirstRadio</a> or similar functions, or from a call to the <b>SetupDiEnumDeviceInterfaces</b> function.

### -param pbtdi

A pointer to a <a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_info_struct">BLUETOOTH_DEVICE_INFO</a> structure into which data about the first Bluetooth device will be placed. For more information, see Remarks.

## -returns

Returns <b>ERROR_SUCCESS</b> upon success, indicating that data about the remote Bluetooth device was retrieved. Returns error codes upon failure. The following table lists common error codes associated with the <b>BluetoothGetDeviceInfo</b> function.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_REVISION_MISMATCH</b></dt>
</dl>
</td>
<td width="60%">
The size of the BLUETOOTH_DEVICE_INFO is not compatible. Check
the <b>dwSize</b> member of the <a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_info_struct">BLUETOOTH_DEVICE_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The radio is not known by the system, or the <b>Address</b> member of the <a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_info_struct">BLUETOOTH_DEVICE_INFO</a> structure is all zeros.

</td>
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
</table>

## -remarks

The Bluetooth device for which data is obtained must have been previously identified through a successful device inquiry function call.

In the <a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_info_struct">BLUETOOTH_DEVICE_INFO</a> structure pointed to by <i>pbtdi</i>, the  <b>dwSize</b> member must be equivalent to the size, in bytes, of the structure. The <b>Address</b>          member of the <b>BLUETOOTH_DEVICE_INFO</b> structure must contain the Bluetooth address of the remote
device.

## -see-also

<a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_info_struct">BLUETOOTH_DEVICE_INFO</a>



<a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_search_params">BLUETOOTH_DEVICE_SEARCH_PARAMS</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothdisplaydeviceproperties">BluetoothDisplayDeviceProperties</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothfinddeviceclose">BluetoothFindDeviceClose</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothfindfirstdevice">BluetoothFindFirstDevice</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothfindnextdevice">BluetoothFindNextDevice</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothremovedevice">BluetoothRemoveDevice</a>
