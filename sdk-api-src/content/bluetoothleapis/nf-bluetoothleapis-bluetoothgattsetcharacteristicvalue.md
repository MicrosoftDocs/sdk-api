---
UID: NF:bluetoothleapis.BluetoothGATTSetCharacteristicValue
title: BluetoothGATTSetCharacteristicValue function (bluetoothleapis.h)
description: Writes the specified characteristic value to the Bluetooth device.
helpviewer_keywords: ["BluetoothGATTSetCharacteristicValue","BluetoothGATTSetCharacteristicValue function [Bluetooth Devices]","bltooth.bluetoothgattsetcharacteristicvalue","bluetoothleapis/BluetoothGATTSetCharacteristicValue"]
old-location: bltooth\bluetoothgattsetcharacteristicvalue.htm
tech.root: bltooth
ms.assetid: 114C1FCD-95F8-4358-8178-C9B283CA7323
ms.date: 12/05/2018
ms.keywords: BluetoothGATTSetCharacteristicValue, BluetoothGATTSetCharacteristicValue function [Bluetooth Devices], bltooth.bluetoothgattsetcharacteristicvalue, bluetoothleapis/BluetoothGATTSetCharacteristicValue
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
 - BluetoothGATTSetCharacteristicValue
 - bluetoothleapis/BluetoothGATTSetCharacteristicValue
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
 - BluetoothGATTSetCharacteristicValue
---

# BluetoothGATTSetCharacteristicValue function


## -description

The <b>BluetoothGATTSetCharacteristicValue</b> function writes the specified characteristic value to the Bluetooth device.

## -parameters

### -param hDevice [in]

Handle to the service.

### -param Characteristic [in]

Pointer to <a href="/windows/desktop/api/bthledef/ns-bthledef-bth_le_gatt_characteristic">BTH_LE_GATT_CHARACTERISTIC</a> structure containing the parent characteristic.

### -param CharacteristicValue [in]

Pointer to <a href="/windows/desktop/api/bthledef/ns-bthledef-bth_le_gatt_characteristic_value">BTH_LE_GATT_CHARACTERISTIC_VALUE</a> structure containing the characteristic value.

### -param ReliableWriteContext [in, optional]

BTH_LE_GATT_RELIABLE_WRITE_CONTEXT structure containing the context describing the reliable write operation returned from a previous call to <a href="/windows/desktop/api/bluetoothleapis/nf-bluetoothleapis-bluetoothgattbeginreliablewrite">BluetoothGATTBeginReliableWrite</a>.

### -param Flags [in]

Flags to modify the behavior of BluetoothGATTSetCharacteristicValue:

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
<tr>
<td>
<b>BLUETOOTH_GATT_FLAG_CONNECTION_ENCRYPTED</b>

</td>
<td>
The client requests the data to be transmitted over an encrypted channel.

</td>
</tr>
<tr>
<td>
<b>BLUETOOTH_GATT_FLAG_CONNECTION_AUTHENTICATED</b>

</td>
<td>
The client requests the data to be transmitted over an authenticated channel.

</td>
</tr>
<tr>
<td>
<b>BLUETOOTH_GATT_FLAG_WRITE_WITHOUT_RESPONSE</b>

</td>
<td>
Write without response.

</td>
</tr>
<tr>
<td>
<b>BLUETOOTH_GATT_FLAG_SIGNED_WRITE</b>

</td>
<td>
Signed write. Profile drivers must use with <b>BLUETOOTH_GATT_FLAG_WRITE_WITHOUT_RESPONSE</b> in order to produce signed write without a response.

</td>
</tr>
</table>

## -returns

The <b>BluetoothGATTSetCharacteristicValue</b> function returns the following values:

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
<dt><b>ERROR_INVALID_FUNCTION</b></dt>
</dl>
</td>
<td width="60%">
A reliable write operation is already presently underway.

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

## -remarks

Calling <b>BluetoothGATTSetCharacteristicValue</b> after <a href="/windows/desktop/api/bluetoothleapis/nf-bluetoothleapis-bluetoothgattbeginreliablewrite">BluetoothGATTBeginReliableWrite</a>, notifies the remote Bluetooth device to store this request into a prepare queue on the device.

If signing is required, then the operation must not require a response, and must not occur over a secure channel.

The parent characteristic is returned from a previous call to <a href="/windows/desktop/api/bluetoothleapis/nf-bluetoothleapis-bluetoothgattgetcharacteristics">BluetoothGATTGetCharacteristics</a>, and must not be altered.  Behavior is undefined
    if the caller does this.

<b>Example</b>


```cpp

BTH_LE_GATT_CHARACTERISTIC_VALUE newValue;

RtlZeroMemory(&newValue,(sizeof(newValue)));

newValue.DataSize = sizeof(valueData);
newValue.Data = (UCHAR*)&valueData;

// Set the new characteristic value
hr = BluetoothGATTSetCharacteristicValue(hDevice,
                                    parentCharacteristic,
                                    &newValue,
                                    NULL,
                                    BLUETOOTH_GATT_FLAG_NONE);

```

## -see-also

<a href="/windows/desktop/api/bthledef/ns-bthledef-bth_le_gatt_characteristic">BTH_LE_GATT_CHARACTERISTIC</a>



<a href="/windows/desktop/api/bthledef/ns-bthledef-bth_le_gatt_characteristic_value">BTH_LE_GATT_CHARACTERISTIC_VALUE</a>