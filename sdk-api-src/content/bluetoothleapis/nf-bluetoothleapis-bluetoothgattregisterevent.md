---
UID: NF:bluetoothleapis.BluetoothGATTRegisterEvent
title: BluetoothGATTRegisterEvent function (bluetoothleapis.h)
description: Registers a routine to be called back during a characteristic value change event on the given characteristic identified by its characteristic handle.
helpviewer_keywords: ["BluetoothGATTRegisterEvent","BluetoothGATTRegisterEvent function [Bluetooth Devices]","bltooth.bluetoothgattregisterevent","bluetoothleapis/BluetoothGATTRegisterEvent"]
old-location: bltooth\bluetoothgattregisterevent.htm
tech.root: bltooth
ms.assetid: 8C1477F8-8342-4405-8FE1-8109E6147EE9
ms.date: 12/05/2018
ms.keywords: BluetoothGATTRegisterEvent, BluetoothGATTRegisterEvent function [Bluetooth Devices], bltooth.bluetoothgattregisterevent, bluetoothleapis/BluetoothGATTRegisterEvent
req.header: bluetoothleapis.h
req.include-header: 
req.target-type: Universal
req.target-min-winverclnt: Supported in Windows 8 and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: BluetoothApis.lib
req.dll: BluetoothAPIs.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BluetoothGATTRegisterEvent
 - bluetoothleapis/BluetoothGATTRegisterEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - BluetoothAPIs.dll
 - Ext-MS-Win-Bluetooth-APIs-l1-1-0.dll
api_name:
 - BluetoothGATTRegisterEvent
---

# BluetoothGATTRegisterEvent function


## -description

The <b>BluetoothGATTRegisterEvent</b> function registers a routine to be called back during a characteristic value change event on the given characteristic identified by its characteristic handle.

## -parameters

### -param hService [in]

Handle to the service.

### -param EventType [in]

A value from <a href="/windows/desktop/api/bthledef/ne-bthledef-bth_le_gatt_event_type">BTH_LE_GATT_EVENT_TYPE</a>. Currently, only <b>CharacteristicValueChangedEvent</b> is supported.

### -param EventParameterIn [in]

Pointer to a <a href="/windows/win32/api/bthledef/ns-bthledef-bluetooth_gatt_value_changed_event_registration">BLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION</a> structure to pass when the event is triggered.

### -param Callback [in]

The routine to call when the Characteristic value changes.

### -param CallbackContext [in, optional]

Context to pass to <i>Callback</i>.

### -param pEventHandle [out]

Pointer to buffer to receive a handle for the registration.  Profile drivers must pass this handle when calling <a href="/windows/desktop/api/bluetoothleapis/nf-bluetoothleapis-bluetoothgattunregisterevent">BluetoothGATTUnregisterEvent</a>.

### -param Flags [in]

Flags to modify the behavior of <b>BluetoothGATTRegisterEvent</b>:

<table>
<tr>
<th>Flag</th>
<th>Description</th>
</tr>
<tr>
<td>
<b>BLUETOOTH_GATT_FLAG_NONE</b>

</td>
<td>
The client does not have specific GATT requirements (default).

</td>
</tr>
</table>

## -returns

<b>BluetoothGATTRegisterEvent</b> returns the following values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The operation completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Returned if both a parent service and a service handle are provided and the service hierarchy does not roll up to the provided parent service handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter was invalid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/win32/api/bthledef/ns-bthledef-bluetooth_gatt_value_changed_event_registration">BLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION</a>



<a href="/windows/desktop/api/bthledef/ne-bthledef-bth_le_gatt_event_type">BTH_LE_GATT_EVENT_TYPE</a>



<a href="/windows/desktop/api/bthledef/nc-bthledef-pfnbluetooth_gatt_event_callback">Bluetooth GATT Event Callback Function</a>



<a href="/windows/desktop/api/bluetoothleapis/nf-bluetoothleapis-bluetoothgattunregisterevent">BluetoothGATTUnregisterEvent</a>