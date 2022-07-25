---
UID: NF:bluetoothapis.BluetoothFindNextDevice
title: BluetoothFindNextDevice function (bluetoothapis.h)
description: The BluetoothFindNextDevice function finds the next Bluetooth device.
helpviewer_keywords: ["BluetoothFindNextDevice","BluetoothFindNextDevice function [Bluetooth]","bluetooth.bluetoothfindnextdevice","bluetoothapis/BluetoothFindNextDevice"]
old-location: bluetooth\bluetoothfindnextdevice.htm
tech.root: bluetooth
ms.assetid: a17d87b2-91d7-4a03-bff7-9bc0ee48c3b4
ms.date: 12/05/2018
ms.keywords: BluetoothFindNextDevice, BluetoothFindNextDevice function [Bluetooth], bluetooth.bluetoothfindnextdevice, bluetoothapis/BluetoothFindNextDevice
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
 - BluetoothFindNextDevice
 - bluetoothapis/BluetoothFindNextDevice
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
 - BluetoothFindNextDevice
---

# BluetoothFindNextDevice function


## -description

The <b>BluetoothFindNextDevice</b> function finds the next  Bluetooth device.

## -parameters

### -param hFind

Handle for the query obtained in a previous call to the <a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothfindfirstdevice">BluetoothFindFirstDevice</a> function.

### -param pbtdi

Pointer to a <a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_info_struct">BLUETOOTH_DEVICE_INFO</a> structure into which information about the next Bluetooth device found is placed. The <b>dwSize</b> member of the <b>BLUETOOTH_DEVICE_INFO</b> structure pointed to by <i>pbtdi</i> must match the size of the structure, or the call to <b>BluetoothFindNextDevice</b> fails.

## -returns

Returns <b>TRUE</b> when the next device is successfully found, and the <i>pbtdi</i> parameter points to information about the device. Returns <b>FALSE</b> upon error. Call the  <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function for more information on the error. The following table  describe common errors:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
No more devices were found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

</td>
</tr>
</table>

## -see-also

<a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_info_struct">BLUETOOTH_DEVICE_INFO</a>



<a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_search_params">BLUETOOTH_DEVICE_SEARCH_PARAMS</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothdisplaydeviceproperties">BluetoothDisplayDeviceProperties</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothfinddeviceclose">BluetoothFindDeviceClose</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothfindfirstdevice">BluetoothFindFirstDevice</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothgetdeviceinfo">BluetoothGetDeviceInfo</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothremovedevice">BluetoothRemoveDevice</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothupdatedevicerecord">BluetoothUpdateDeviceRecord</a>