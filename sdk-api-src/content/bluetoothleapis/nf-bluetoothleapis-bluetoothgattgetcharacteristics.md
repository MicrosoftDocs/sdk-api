---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# BluetoothGATTGetCharacteristics function


## -description


The <b>BluetoothGATTGetCharacteristics</b> function gets all the characteristics available for the specified service.


## -parameters




### -param hDevice [in]

Handle to the Bluetooth device or service.


### -param Service [in, optional]

Address of a <a href="https://msdn.microsoft.com/library/windows/hardware/hh450850">BTH_LE_GATT_SERVICE</a> structure containing the parent service of the included services to be retrieved. This parameter is required if a device handle is passed to <i>hDevice</i>. This parameter is optional if a service handle was passed to <i>hDevice</i>, in which case the service specified by the service handle will be treated as the parent.


### -param CharacteristicsBufferCount [in]

The number of elements allocated for the <i>CharacteristicsBuffer</i> parameter.


### -param CharacteristicsBuffer [out, optional]

Pointer to buffer into which to return characteristics in a <a href="https://msdn.microsoft.com/library/windows/hardware/hh450850">BTH_LE_GATT_SERVICE</a> structure.


### -param CharacteristicsBufferActual [out]

Pointer to buffer into which the actual number of characteristics were returned in the <i>CharacteristicsBuffer</i> parameter.


### -param Flags [in]

Flags to modify the behavior of <b>BluetoothGATTGetCharacteristics</b>:

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
<li><i>CharacteristicsBuffer</i> is <b>NULL</b>, and <i>CharacteristicsBufferCount</i> is 0</li>
<li><i>CharacteristicsBuffer</i> is non-<b>NULL</b>, but <i>CharacteristicsBufferCount</i> is <b>NULL</b></li>
<li><i>CharacteristicsBuffer</i> is non-<b>NULL</b>, and <i>CharacteristicsBufferCount</i> is 0</li>
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
    characteristics to be returned in.  Callers can determine the necessary buffer size by passing a non-<b>NULL</b> value in <i>CharacteristicsBufferActual</i> and <b>NULL</b> in <i>CharacteristicsBuffer</i>.

Do not modify the returned characteristic structure,
    and then use the modified  structure in subsequent function calls.  Behavior is undefined
    if the caller does this.

The parent service must be present in the
    cache, otherwise the function will fail.  The parent service must be a service returned by either <a href="https://msdn.microsoft.com/library/windows/hardware/hh450802">BluetoothGATTGetServices</a> or
    <a href="https://msdn.microsoft.com/library/windows/hardware/hh450800">BluetoothGATTGetIncludedServices</a>.

<b>Example</b>

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>////////////////////////////////////////////////////////////////////////////
// Determine Characteristic Buffer Size
////////////////////////////////////////////////////////////////////////////

        hr = BluetoothGATTGetCharacteristics(
                hCurrService,
                currGattService,
                0,
                NULL,
                &amp;charBufferSize,
                BLUETOOTH_GATT_FLAG_NONE);
        
        if (HRESULT_FROM_WIN32(ERROR_MORE_DATA) != hr) {
            PrintHr("BluetoothGATTGetCharacteristics - Buffer Size", hr);
            goto Done;
        }
        
        if (charBufferSize &gt; 0) {
            pCharBuffer = (PBTH_LE_GATT_CHARACTERISTIC)
                    malloc(charBufferSize * sizeof(BTH_LE_GATT_CHARACTERISTIC));
        
            if (NULL == pCharBuffer) {
                printf("pCharBuffer out of memory\r\n");
                goto Done;
            } else {
                RtlZeroMemory(pCharBuffer, 
                        charBufferSize * sizeof(BTH_LE_GATT_CHARACTERISTIC));
            }

////////////////////////////////////////////////////////////////////////////
// Retrieve Characteristics
////////////////////////////////////////////////////////////////////////////
    
            hr = BluetoothGATTGetCharacteristics(
                    hCurrService,
                    currGattService,
                    charBufferSize,
                    pCharBuffer,
                    &amp;numChars,
                    BLUETOOTH_GATT_FLAG_NONE);

            if (S_OK != hr) {
                PrintHr("BluetoothGATTGetCharacteristics - Actual Data", hr);
                goto Done; // Allow continuation
            }

            if (numChars != charBufferSize) {
                printf("buffer size and buffer size actual size mismatch\r\n");
                goto Done;
            }
        }</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/hh450840">BTH_LE_GATT_CHARACTERISTIC</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh450850">BTH_LE_GATT_SERVICE</a>
 

 

