---
UID: NF:bluetoothleapis.BluetoothGATTUnregisterEvent
title: BluetoothGATTUnregisterEvent function (bluetoothleapis.h)
description: Unregisters the given characteristic value change event.
helpviewer_keywords: ["BluetoothGATTUnregisterEvent","BluetoothGATTUnregisterEvent function [Bluetooth Devices]","bltooth.bluetoothgattunregisterevent","bluetoothleapis/BluetoothGATTUnregisterEvent"]
old-location: bltooth\bluetoothgattunregisterevent.htm
tech.root: bltooth
ms.assetid: 4E0E8D6C-DC12-4F15-9D29-B38AE680894B
ms.date: 12/05/2018
ms.keywords: BluetoothGATTUnregisterEvent, BluetoothGATTUnregisterEvent function [Bluetooth Devices], bltooth.bluetoothgattunregisterevent, bluetoothleapis/BluetoothGATTUnregisterEvent
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
req.lib: BluetoothAPIs.lib
req.dll: BluetoothAPIs.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BluetoothGATTUnregisterEvent
 - bluetoothleapis/BluetoothGATTUnregisterEvent
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
 - BluetoothGATTUnregisterEvent
---

# BluetoothGATTUnregisterEvent function


## -description

The <b>BluetoothGATTUnregisterEvent</b> function unregisters the given characteristic value change event.

## -parameters

### -param EventHandle [in]

Handle returned from a previous call to <a href="/windows/desktop/api/bluetoothleapis/nf-bluetoothleapis-bluetoothgattregisterevent">BluetoothGATTRegisterEvent</a>.

### -param Flags [in]

Flags to modify the behavior of <b>BluetoothGATTUnregisterEvent</b>:

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

<b>BluetoothGATTUnregisterEvent</b> returns the following values:

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

<a href="/windows/desktop/api/bluetoothleapis/nf-bluetoothleapis-bluetoothgattregisterevent">BluetoothGATTRegisterEvent</a>