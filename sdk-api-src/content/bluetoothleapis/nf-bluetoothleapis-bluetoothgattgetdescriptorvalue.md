---
UID: NF:bluetoothleapis.BluetoothGATTGetDescriptorValue
title: BluetoothGATTGetDescriptorValue function (bluetoothleapis.h)
description: Gets the value of the specified descriptor.
helpviewer_keywords: ["BluetoothGATTGetDescriptorValue","BluetoothGATTGetDescriptorValue function [Bluetooth Devices]","bltooth.bluetoothgattgetdescriptorvalue","bluetoothleapis/BluetoothGATTGetDescriptorValue"]
old-location: bltooth\bluetoothgattgetdescriptorvalue.htm
tech.root: bltooth
ms.assetid: 06820384-7098-415A-A350-3A755162FAA3
ms.date: 12/05/2018
ms.keywords: BluetoothGATTGetDescriptorValue, BluetoothGATTGetDescriptorValue function [Bluetooth Devices], bltooth.bluetoothgattgetdescriptorvalue, bluetoothleapis/BluetoothGATTGetDescriptorValue
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
 - BluetoothGATTGetDescriptorValue
 - bluetoothleapis/BluetoothGATTGetDescriptorValue
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
 - BluetoothGATTGetDescriptorValue
---

# BluetoothGATTGetDescriptorValue function


## -description

The <b>BluetoothGATTGetDescriptorValue</b> function gets the value of the specified descriptor.

## -parameters

### -param hDevice [in]

Handle to the service.

### -param Descriptor [in]

Pointer to <a href="/windows/desktop/api/bthledef/ns-bthledef-bth_le_gatt_descriptor">BTH_LE_GATT_DESCRIPTOR</a> structure containing the parent descriptor of the descriptor value to be retrieved.

### -param DescriptorValueDataSize [in]

The number of bytes allocated for the <i>DescriptorValue</i> parameter.

### -param DescriptorValue [out, optional]

Pointer to <a href="/windows/desktop/api/bthledef/ns-bthledef-bth_le_gatt_descriptor_value">BTH_LE_GATT_DESCRIPTOR_VALUE</a> structure into which to return the descriptor value.

### -param DescriptorValueSizeRequired [out, optional]

Pointer to buffer into which to store the number of additional bytes needed to return data in the buffer pointed to by <i>DescriptorValue</i>.

### -param Flags [in]

Flags to modify the behavior of <b>BluetoothGATTGetDescriptorValue</b>:

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
<b>BLUETOOTH_GATT_FLAG_FORCE_READ_FROM_DEVICE</b>

</td>
<td>
The descriptor value is to be read directly from the device.  This overwrites the one in the cache if one is already present.

</td>
</tr>
<tr>
<td>
<b>BLUETOOTH_GATT_FLAG_FORCE_READ_FROM_CACHE</b>

</td>
<td>
The descriptor value is to be read from the cache (regardless of whether it is present in the cache or not).

</td>
</tr>
</table>

## -returns

The <b>BluetoothGATTGetDescriptorValue</b> function returns the following values:

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
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The buffer parameter is <b>NULL</b> and the number of items available is being returned instead.

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
Both <i>DescriptorValue</i> and <i>DescriptorValueSizeRequired</i> are 0.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_USER_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
A buffer is specified, but the buffer count
            size is smaller than what is required, in bytes.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_FUNCTION</b></dt>
</dl>
</td>
<td width="60%">
A descriptor value was specified to be retrieved from
            the cache, but the descriptor value is not present in the cache.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_COMMAND</b></dt>
</dl>
</td>
<td width="60%">
The current data in the cache appears to be
            inconsistent, and is leading to internal errors.

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

## -remarks

The descriptor value is returned from the cache if one is already present. This would be the case most of the time, as all the device attributes are cached at the time of pairing or association.  However, if it is not present, the descriptor value is read directly from the device, and will be cached upon successfully reading it from the device.  If <b>BLUETOOTH_GATT_FLAG_FORCE_READ_FROM_CACHE</b> or <b>BLUETOOTH_GATT_FLAG_FORCE_READ_FROM_DEVICE</b> is present, the descriptor value is read using the specified method.

Returned descriptor values are cached upon successful retrieval of descriptor values from the device directly.  Unless a service-change event is received, the descriptor values is not expected to change.

Profile drivers should pre-allocate  a sufficiently large buffer for the array of
    descriptor values to be returned in.  Callers can determine the necessary buffer size by passing a non-<b>NULL</b> value in <i>DescriptorValueSizeRequired</i> and <b>NULL</b> in <i>DescriptorValue</i>.

The parent service must be present in the
    cache, otherwise the function will fail.  The parent service must be a service returned by either <a href="/windows/desktop/api/bluetoothleapis/nf-bluetoothleapis-bluetoothgattgetservices">BluetoothGATTGetServices</a> or
    <a href="/windows/desktop/api/bluetoothleapis/nf-bluetoothleapis-bluetoothgattgetincludedservices">BluetoothGATTGetIncludedServices</a>.

<b>Example</b>


```cpp

////////////////////////////////////////////////////////////////////////////
// Determine Descriptor Value Buffer Size
////////////////////////////////////////////////////////////////////////////
                hr = BluetoothGATTGetDescriptorValue(
                        hCurrService,
                        currGattDescriptor,
                        0,
                        NULL,
                        &descValueDataSize,
                        BLUETOOTH_GATT_FLAG_NONE);

                if (HRESULT_FROM_WIN32(ERROR_MORE_DATA) != hr) {
                    PrintHr("BluetoothGATTGetDescriptorValue - Buffer Size", hr);
                    goto Done; // allow continuation
                }

                pDescValueBuffer = (PBTH_LE_GATT_DESCRIPTOR_VALUE)malloc(descValueDataSize);

                if (NULL == pDescValueBuffer) {
                    printf("pDescValueBuffer out of memory\r\n");
                    goto Done;
                } else {
                    RtlZeroMemory(pDescValueBuffer, descValueDataSize);
                }

////////////////////////////////////////////////////////////////////////////
// Retrieve the Descriptor Value
////////////////////////////////////////////////////////////////////////////

                hr = BluetoothGATTGetDescriptorValue(
                        hCurrService,
                        currGattDescriptor,
                        (ULONG)descValueDataSize,
                        pDescValueBuffer,
                        NULL,
                        BLUETOOTH_GATT_FLAG_NONE);

                if (S_OK != hr) {
                    PrintHr("BluetoothGATTGetDescriptorValue - Actual Data", hr);
                    goto Done; // allow continuation
                }

```

## -see-also

<a href="/windows/desktop/api/bthledef/ns-bthledef-bth_le_gatt_descriptor">BTH_LE_GATT_DESCRIPTOR</a>



<a href="/windows/desktop/api/bthledef/ns-bthledef-bth_le_gatt_descriptor_value">BTH_LE_GATT_DESCRIPTOR_VALUE</a>