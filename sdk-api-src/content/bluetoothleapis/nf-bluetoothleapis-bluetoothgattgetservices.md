---
UID: NF:bluetoothleapis.BluetoothGATTGetServices
title: BluetoothGATTGetServices function
author: windows-sdk-content
description: The BluetoothGATTGetServices function gets all the primary services available for a server.
old-location: bltooth\bluetoothgattgetservices.htm
old-project: bltooth
ms.assetid: 8EF8B582-FFAE-4C87-8E94-7EFDD2CD2706
ms.author: windowssdkdev
ms.date: 04/30/2018
ms.keywords: BluetoothGATTGetServices, BluetoothGATTGetServices function [Bluetooth Devices], bltooth.bluetoothgattgetservices, bluetoothleapis/BluetoothGATTGetServices
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: SDP_STRING_TYPE_DATA, *PSDP_STRING_TYPE_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - BluetoothAPIs.dll
 - Ext-MS-Win-Bluetooth-APIs-l1-1-0.dll
api_name:
 - BluetoothGATTGetServices
product: Windows
targetos: Windows
req.lib: BluetoothAPIs.lib
req.dll: BluetoothAPIs.dll
req.irql: 
---

# BluetoothGATTGetServices function


## -description


The <b>BluetoothGATTGetServices</b> function gets all the primary services available for a server.


## -parameters




### -param hDevice [in]

Handle to the Bluetooth device from which to obtain the list of primary services.


### -param ServicesBufferCount [in]

The number of elements allocated for the <i>ServicesBuffer</i> parameter.


### -param ServicesBuffer [out, optional]

Pointer to buffer containing a <a href="https://msdn.microsoft.com/library/windows/hardware/hh450850">BTH_LE_GATT_SERVICE</a> structure into which to return services.


### -param ServicesBufferActual [out]

Pointer to buffer into which the actual number of services were returned in the <i>ServicesBuffer</i> parameter.


### -param Flags [in]

Flags to modify the behavior of <b>BluetoothGATTGetServices</b>:

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
<li><i>ServicesBuffer</i> is <b>NULL</b>, and <i>ServicesBufferCount</i> is 0</li>
<li><i>ServicesBuffer</i> is non-<b>NULL</b>, but <i>ServicesBufferCount</i> is <b>NULL</b></li>
<li><i>ServicesBuffer</i> is non-<b>NULL</b>, and <i>ServicesBufferCount</i> is 0</li>
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
    primary services to be returned in.  Callers can determine the necessary buffer size by passing a non-<b>NULL</b> value in <i>ServicesBufferActual</i> and <b>NULL</b> in <i>ServicesBuffer</i>.

Do not modify the returned service structure,
    and then use the modified structure in subsequent function calls.  Behavior is undefined
    if the caller does this.

<b>Example</b>

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
////////////////////////////////////////////////////////////////////////////
// Determine Services Buffer Size
////////////////////////////////////////////////////////////////////////////

    hr = BluetoothGATTGetServices(
            hLEDevice,
            0,
            NULL,
            &amp;serviceBufferCount,
            BLUETOOTH_GATT_FLAG_NONE);
    
    if (HRESULT_FROM_WIN32(ERROR_MORE_DATA) != hr) {
        PrintHr("BluetoothGATTGetServices - Buffer Size", hr);
        goto Done;
    }

    pServiceBuffer = (PBTH_LE_GATT_SERVICE)
            malloc(sizeof(BTH_LE_GATT_SERVICE) * serviceBufferCount);
    
    if (NULL == pServiceBuffer) {
        printf("pServiceBuffer out of memory\r\n");
        goto Done;
    } else {
        RtlZeroMemory(pServiceBuffer, 
                sizeof(BTH_LE_GATT_SERVICE) * serviceBufferCount);
    }
    
////////////////////////////////////////////////////////////////////////////
// Retrieve Services
////////////////////////////////////////////////////////////////////////////
    
    hr = BluetoothGATTGetServices(
            hLEDevice,
            serviceBufferCount,
            pServiceBuffer,
            &amp;numServices,
            BLUETOOTH_GATT_FLAG_NONE);
    
    if (S_OK != hr) {
        PrintHr("BluetoothGATTGetServices - Actual Data", hr);
        goto Done;
    }
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/hh450850">BTH_LE_GATT_SERVICE</a>
 

 

