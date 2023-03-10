---
UID: NF:bluetoothleapis.BluetoothGATTGetIncludedServices
title: BluetoothGATTGetIncludedServices function (bluetoothleapis.h)
description: Gets all the included services available for a given service.
helpviewer_keywords: ["BluetoothGATTGetIncludedServices","BluetoothGATTGetIncludedServices function [Bluetooth Devices]","bltooth.bluetoothgattgetincludedservices","bluetoothleapis/BluetoothGATTGetIncludedServices"]
old-location: bltooth\bluetoothgattgetincludedservices.htm
tech.root: bltooth
ms.assetid: 72F0E995-88B6-42E0-9B69-429566B5605C
ms.date: 12/05/2018
ms.keywords: BluetoothGATTGetIncludedServices, BluetoothGATTGetIncludedServices function [Bluetooth Devices], bltooth.bluetoothgattgetincludedservices, bluetoothleapis/BluetoothGATTGetIncludedServices
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
 - BluetoothGATTGetIncludedServices
 - bluetoothleapis/BluetoothGATTGetIncludedServices
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
 - BluetoothGATTGetIncludedServices
---

# BluetoothGATTGetIncludedServices function


## -description

The <b>BluetoothGATTGetIncludedServices</b> function gets all the included services available for a given service.

## -parameters

### -param hDevice [in]

Handle to the Bluetooth device or parent service.

### -param ParentService [in, optional]

Address of a <a href="/windows/desktop/api/bthledef/ns-bthledef-bth_le_gatt_service">BTH_LE_GATT_SERVICE</a> structure that contains the parent service of the included services to be retrieved. This parameter is required if a device handle is passed to <i>hDevice</i>. This parameter is optional if a service handle was passed to <i>hDevice</i>, in which case the service specified by the service handle will be treated as the parent.

### -param IncludedServicesBufferCount [in]

The number of elements allocated for the <i>IncludedServicesBuffer</i> parameter.

### -param IncludedServicesBuffer [out, optional]

Address of a buffer containing a <a href="/windows/desktop/api/bthledef/ns-bthledef-bth_le_gatt_service">BTH_LE_GATT_SERVICE</a> structure into which to return included services.

### -param IncludedServicesBufferActual [out]

Pointer to buffer into which the actual number of included services were returned in the <i>IncludedServicesBuffer</i> parameter.

### -param Flags [in]

Flags to modify the behavior of <b>BluetoothGATTGetIncludedServices</b>:

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
One of the following conditions occurred:

<ul>
<li><i>IncludedServicesBuffer</i> is <b>NULL</b>, and <i>IncludedServicesBufferCount</i> is 0.</li>
<li><i>IncludedServicesBuffer</i> is non-<b>NULL</b>, but <i>IncludedServicesBufferCount</i> is <b>NULL</b>.</li>
<li><i>IncludedServicesBuffer</i> is non-<b>NULL</b>, and <i>IncludedServicesBufferCount</i> is 0.</li>
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
<dt><b>ERROR_INVALID_FUNCTION</b></dt>
</dl>
</td>
<td width="60%">
Services were specified to be retrieved from
            the cache, but no services are present in the cache.

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

Returned services are cached upon successful retrieval of services from the device directly.  Unless a service-change event is received, the list of returned services is not expected to change.

Profile drivers should pre-allocate  a sufficiently large buffer for the array of
    primary services to be returned in.  Callers can determine the necessary buffer size by passing a non-<b>NULL</b> value in <i>IncludedServicesBufferActual</i> and <b>NULL</b> in <i>IncludedServicesBuffer</i>.

Do not modify the returned service structure,
    and then use the modified structure in subsequent function calls.  Behavior is undefined
    if the caller does this.

<b>Example</b>


```cpp

////////////////////////////////////////////////////////////////////////////
// Determine Included Services Buffer Size
////////////////////////////////////////////////////////////////////////////
hr = BluetoothGATTGetIncludedServices(
     hLEDevice,
     gattService,
     0,
     NULL,
     &inclServicesBufferSize,
     BLUETOOTH_GATT_FLAG_NONE);

     if (HRESULT_FROM_WIN32(ERROR_MORE_DATA) != hr) {
         PrintHr("BluetoothGATTGetIncludedServices - Buffer Size", hr);
         goto Done;
     }

     if (inclServicesBufferSize > 0) {
         pInclServicesBuffer = (PBTH_LE_GATT_ PBTH_LE_GATT_SERVICE)
                    malloc(inclServicesBufferSize * sizeof(BTH_LE_GATT_SERVICE));

         if (NULL == pInclServicesBuffer) {
             printf("pInclServicesBuffer out of memory\r\n");
             goto Done;
         } else {
             RtlZeroMemory(pInclServicesBuffer, 
                    inclServicesBufferSize * sizeof(BTH_LE_GATT_SERVICE));
         }

         ////////////////////////////////////////////////////////////////////////////
         // Retrieve Included Services
         ////////////////////////////////////////////////////////////////////////////

         hr = BluetoothGATTGetIncludedServices (
              hLEDevice,
              gattService,
              inclServicesBufferSize,
              pInclServicesBuffer,
              &numIncludedServices
              BLUETOOTH_GATT_FLAG_NONE);

         if (S_OK != hr) {
             PrintHr("BluetoothGATTGetIncludedServices - Actual Data", hr);
             goto Done;
         }
     }
```

## -see-also

<a href="/windows/desktop/api/bthledef/ns-bthledef-bth_le_gatt_service">BTH_LE_GATT_SERVICE</a>