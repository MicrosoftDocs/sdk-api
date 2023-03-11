---
UID: NF:bluetoothapis.BluetoothSetServiceState
title: BluetoothSetServiceState function (bluetoothapis.h)
description: Enables or disables services for a Bluetooth device.
helpviewer_keywords: ["BluetoothSetServiceState","BluetoothSetServiceState function [Bluetooth]","bluetooth.bluetoothsetservicestate","bluetoothapis/BluetoothSetServiceState"]
old-location: bluetooth\bluetoothsetservicestate.htm
tech.root: bluetooth
ms.assetid: 9c68139c-6f55-4b5a-bea0-64681e32a7c5
ms.date: 12/05/2018
ms.keywords: BluetoothSetServiceState, BluetoothSetServiceState function [Bluetooth], bluetooth.bluetoothsetservicestate, bluetoothapis/BluetoothSetServiceState
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
 - BluetoothSetServiceState
 - bluetoothapis/BluetoothSetServiceState
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
 - BluetoothSetServiceState
---

# BluetoothSetServiceState function


## -description

The <b>BluetoothSetServiceState</b> function enables or disables services for a Bluetooth device.

## -parameters

### -param hRadio

A handle of the local Bluetooth radio.

### -param pbtdi

A pointer to a <a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_info_struct">BLUETOOTH_DEVICE_INFO</a> structure. Must be a previously found radio address.

### -param pGuidService

A pointer to the service GUID on the remote device.

### -param dwServiceFlags

The flags that adjust the service. To disable the service, set to <b>BLUETOOTH_SERVICE_DISABLE</b>; to enable the service, set to <b>BLUETOOTH_SERVICE_ENABLE</b>.

## -returns

Returns <b>ERROR_SUCCESS</b> upon successful completion. The following table  lists common errors.

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
The <i>dwServiceFlags</i> are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SERVICE_DOES_NOT_EXIST</b></dt>
</dl>
</td>
<td width="60%">
The GUID specified in <i>pGuidService</i> is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>dwServiceFlags</i>  is set to <b>BLUETOOTH_SERVICE_DISABLE</b> and the service is already disabled, or <i>dwServiceFlags</i>  is set to  <b>BLUETOOTH_SERVICE_ENABLE</b> and the service is already enabled.

</td>
</tr>
</table>

## -remarks

Windows maintains a mapping of  service Globally Unique Identifiers (GUIDs) to supported drivers for
Bluetooth-enabled devices. Enabling a service installs the corresponding
device driver and disabling a service removes the corresponding device driver.
If a non-supported service is enabled, a driver is not installed.

## -see-also

<a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_info_struct">BLUETOOTH_DEVICE_INFO</a>



<a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_search_params">BLUETOOTH_DEVICE_SEARCH_PARAMS</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothdisplaydeviceproperties">BluetoothDisplayDeviceProperties</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothfinddeviceclose">BluetoothFindDeviceClose</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothfindfirstdevice">BluetoothFindFirstDevice</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothfindnextdevice">BluetoothFindNextDevice</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothgetdeviceinfo">BluetoothGetDeviceInfo</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothremovedevice">BluetoothRemoveDevice</a>