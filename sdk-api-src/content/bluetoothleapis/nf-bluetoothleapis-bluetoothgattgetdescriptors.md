---
UID: NF:bluetoothleapis.BluetoothGATTGetDescriptors
title: BluetoothGATTGetDescriptors function (bluetoothleapis.h)
description: Gets all the descriptors available for the specified characteristic.
helpviewer_keywords: ["BluetoothGATTGetDescriptors","BluetoothGATTGetDescriptors function [Bluetooth Devices]","bltooth.bluetoothgattgetdescriptors","bluetoothleapis/BluetoothGATTGetDescriptors"]
old-location: bltooth\bluetoothgattgetdescriptors.htm
tech.root: bltooth
ms.assetid: C4D51362-5D4E-45CC-8E29-10B201B5673C
ms.date: 12/05/2018
ms.keywords: BluetoothGATTGetDescriptors, BluetoothGATTGetDescriptors function [Bluetooth Devices], bltooth.bluetoothgattgetdescriptors, bluetoothleapis/BluetoothGATTGetDescriptors
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
 - BluetoothGATTGetDescriptors
 - bluetoothleapis/BluetoothGATTGetDescriptors
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
 - BluetoothGATTGetDescriptors
---

# BluetoothGATTGetDescriptors function


## -description

The <b>BluetoothGATTGetDescriptors</b> function gets all the descriptors available for the specified characteristic.

## -parameters

### -param hDevice [in]

Handle to the Bluetooth device or service.  If a service handle is passed, then the service must be the grandparent of the descriptor.

### -param Characteristic [in]

Pointer to <a href="/windows/desktop/api/bthledef/ns-bthledef-bth_le_gatt_characteristic">BTH_LE_GATT_CHARACTERISTIC</a> structure containing the parent characteristic of the descriptors to be retrieved.

### -param DescriptorsBufferCount [in]

The number of elements allocated for the <i>DescriptorsBuffer</i> parameter.

### -param DescriptorsBuffer [out, optional]

Pointer to buffer containing a <a href="/windows/desktop/api/bthledef/ns-bthledef-bth_le_gatt_descriptor">BTH_LE_GATT_DESCRIPTOR</a> structure into which to return descriptors.

### -param DescriptorsBufferActual [out]

Pointer to buffer into which the actual number of descriptors were returned in the <i>DescriptorsBuffer</i> parameter.

### -param Flags [in]

Flags to modify the behavior of <b>BluetoothGATTGetDescriptors</b>:

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

This function returns the following values:

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
The buffer parameter is NULL and the number of items available is being returned instead.

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
One of the following conditions occurred: 

<ul>
<li><i>DescriptorsBuffer</i> is <b>NULL</b>, and <i>DescriptorsBufferCount</i> is 0.</li>
<li><i>DescriptorsBuffer</i> is non-<b>NULL</b>, but <i>DescriptorsBufferCount</i> is <b>NULL</b>.</li>
<li><i>DescriptorsBuffer</i> is non-<b>NULL</b>, and <i>DescriptorsBufferCount</i> is 0.</li>
</ul>
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
<dt><b>ERROR_NO_SYSTEM_RESOURCES</b></dt>
</dl>
</td>
<td width="60%">
The operation ran out of memory.

</td>
</tr>
</table>

## -remarks

Returned characteristics are cached upon successful retrieval of characteristics from the device directly.  Unless a service-change event is received, the list of returned characteristics is not expected to change.

Profile drivers should pre-allocate  a sufficiently large buffer for the array of
    characteristics to be returned in.  Callers can determine the necessary buffer size by passing a non-<b>NULL</b> value in <i>DescriptorsBufferActual</i> and <b>NULL</b> in <i>DescriptorsBuffer</i>.

Do not modify the returned characteristic structure,
    and then use the modified  structure in subsequent function calls.  Behavior is undefined
    if the caller does this.

The parent characteristic must be present in the
    cache, otherwise the function will fail.  The parent service must be a service returned by either <a href="/windows/desktop/api/bluetoothleapis/nf-bluetoothleapis-bluetoothgattgetservices">BluetoothGATTGetServices</a> or
    <a href="/windows/desktop/api/bluetoothleapis/nf-bluetoothleapis-bluetoothgattgetincludedservices">BluetoothGATTGetIncludedServices</a>.

<b>Example</b>


```cpp

////////////////////////////////////////////////////////////////////////////
// Determine Descriptor Buffer Size
////////////////////////////////////////////////////////////////////////////
GetDescriptors:
            hr = BluetoothGATTGetDescriptors(
                    hCurrService,
                    currGattChar,
                    0,
                    NULL,
                    &descriptorBufferSize,
                    BLUETOOTH_GATT_FLAG_NONE);
            
            if (HRESULT_FROM_WIN32(ERROR_MORE_DATA) != hr) {
                PrintHr("BluetoothGATTGetDescriptors - Buffer Size", hr);
                goto Done; // Allow continuation
            }
            
            if (descriptorBufferSize > 0) {
                pDescriptorBuffer = (PBTH_LE_GATT_DESCRIPTOR)
                        malloc(descriptorBufferSize 
                            * sizeof(BTH_LE_GATT_DESCRIPTOR));
            
                if (NULL == pDescriptorBuffer) {
                    printf("pDescriptorBuffer out of memory\r\n");
                    goto Done;
                } else {
                    RtlZeroMemory(pDescriptorBuffer, descriptorBufferSize);
                }
            
////////////////////////////////////////////////////////////////////////////
// Retrieve Descriptors
////////////////////////////////////////////////////////////////////////////
    
                hr = BluetoothGATTGetDescriptors(
                        hCurrService,
                        currGattChar,
                        descriptorBufferSize,
                        pDescriptorBuffer,
                        &numDescriptors,
                        BLUETOOTH_GATT_FLAG_NONE);
            
                if (S_OK != hr) {
                    PrintHr("BluetoothGATTGetDescriptors - Actual Data", hr);
                    goto Done;
                }

                if (numDescriptors != descriptorBufferSize) {
                    printf("buffer size and buffer size actual size mismatch\r\n");
                    goto Done;
                }
            }

```

## -see-also

<a href="/windows/desktop/api/bthledef/ns-bthledef-bth_le_gatt_characteristic">BTH_LE_GATT_CHARACTERISTIC</a>



<a href="/windows/desktop/api/bthledef/ns-bthledef-bth_le_gatt_descriptor">BTH_LE_GATT_DESCRIPTOR</a>