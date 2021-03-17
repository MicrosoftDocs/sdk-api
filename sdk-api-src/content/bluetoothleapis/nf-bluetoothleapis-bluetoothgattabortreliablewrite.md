---
UID: NF:bluetoothleapis.BluetoothGATTAbortReliableWrite
title: BluetoothGATTAbortReliableWrite function (bluetoothleapis.h)
description: Specifies the end of reliable write procedures, and the writes should be aborted.
helpviewer_keywords: ["BluetoothGATTAbortReliableWrite","BluetoothGATTAbortReliableWrite function [Bluetooth Devices]","bltooth.bluetoothgattabortreliablewrite","bluetoothleapis/BluetoothGATTAbortReliableWrite"]
old-location: bltooth\bluetoothgattabortreliablewrite.htm
tech.root: bltooth
ms.assetid: 6EC1D80A-6327-4D5A-8460-87C339669BDA
ms.date: 12/05/2018
ms.keywords: BluetoothGATTAbortReliableWrite, BluetoothGATTAbortReliableWrite function [Bluetooth Devices], bltooth.bluetoothgattabortreliablewrite, bluetoothleapis/BluetoothGATTAbortReliableWrite
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
 - BluetoothGATTAbortReliableWrite
 - bluetoothleapis/BluetoothGATTAbortReliableWrite
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
 - BluetoothGATTAbortReliableWrite
---

# BluetoothGATTAbortReliableWrite function


## -description

The <b>BluetoothGATTAbortReliableWrite</b> function specifies the end of reliable write procedures, and the writes should be aborted.

## -parameters

### -param hDevice [in]

Handle to the service.

### -param ReliableWriteContext [in]

The context describing the reliable write operation returned from a previous call to <a href="/windows/desktop/api/bluetoothleapis/nf-bluetoothleapis-bluetoothgattbeginreliablewrite">BluetoothGATTBeginReliableWrite</a>.

### -param Flags [in]

Flags to modify the behavior of <b>BluetoothGATTAbortReliableWrite</b>:

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

The <b>BluetoothGATTAbortReliableWrite</b> function returns the following values:

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
<dt><b>ERROR_INVALID_FUNCTION</b></dt>
</dl>
</td>
<td width="60%">
A reliable write operation is not presently underway.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_NET_RESP</b></dt>
</dl>
</td>
<td width="60%">
The target server did not provide an
            appropriate network response.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SEM_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The request timed-out.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_SYSTEM_RESOURCES</b></dt>
</dl>
</td>
<td width="60%">
The operation ran out of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_BLUETOOTH_ATT_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The attribute handle given was not valid on this server.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_BLUETOOTH_ATT_READ_NOT_PERMITTED</b></dt>
</dl>
</td>
<td width="60%">
The attribute cannot be read.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_BLUETOOTH_ATT_WRITE_NOT_PERMITTED</b></dt>
</dl>
</td>
<td width="60%">
The attribute cannot be written.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_BLUETOOTH_ATT_INVALID_PDU</b></dt>
</dl>
</td>
<td width="60%">
The attribute PDU was invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_BLUETOOTH_ATT_INSUFFICIENT_AUTHENTICATION</b></dt>
</dl>
</td>
<td width="60%">
The attribute requires authentication before it can be read or written.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_BLUETOOTH_ATT_REQUEST_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
Attribute server does not support the request received from the client.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_BLUETOOTH_ATT_INVALID_OFFSET</b></dt>
</dl>
</td>
<td width="60%">
Offset specified was past the end of the attribute.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_BLUETOOTH_ATT_INSUFFICIENT_AUTHORIZATION</b></dt>
</dl>
</td>
<td width="60%">
The attribute requires authorization before it can be read or written.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_BLUETOOTH_ATT_PREPARE_QUEUE_FULL</b></dt>
</dl>
</td>
<td width="60%">
Too many prepare writes have been queued.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_BLUETOOTH_ATT_ATTRIBUTE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
No attribute found within the given attribute handle range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_BLUETOOTH_ATT_ATTRIBUTE_NOT_LONG</b></dt>
</dl>
</td>
<td width="60%">
The attribute cannot be read or written using the Read Blob Request.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_BLUETOOTH_ATT_INSUFFICIENT_ENCRYPTION_KEY_SIZE</b></dt>
</dl>
</td>
<td width="60%">
The Encryption Key Size used for encrypting this link is insufficient.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_BLUETOOTH_ATT_INVALID_ATTRIBUTE_VALUE_LENGTH</b></dt>
</dl>
</td>
<td width="60%">
The attribute value length is invalid for the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_BLUETOOTH_ATT_UNLIKELY</b></dt>
</dl>
</td>
<td width="60%">
The attribute request that was requested has encountered an error that was unlikely, and therefore could not be completed as requested.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_BLUETOOTH_ATT_INSUFFICIENT_ENCRYPTION</b></dt>
</dl>
</td>
<td width="60%">
The attribute requires encryption before it can be read or written.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_BLUETOOTH_ATT_UNSUPPORTED_GROUP_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The attribute type is not a supported grouping attribute as defined by a higher layer specification.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_BLUETOOTH_ATT_INSUFFICIENT_RESOURCES</b></dt>
</dl>
</td>
<td width="60%">
Insufficient Resources to complete the request.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_BLUETOOTH_ATT_UNKNOWN_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An error that lies in the reserved range has been received.

</td>
</tr>
</table>