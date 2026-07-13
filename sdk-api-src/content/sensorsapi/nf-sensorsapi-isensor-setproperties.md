---
UID: NF:sensorsapi.ISensor.SetProperties
title: ISensor::SetProperties (sensorsapi.h)
description: Specifies sensor properties.
helpviewer_keywords: ["ISensor interface","SetProperties method","ISensor.SetProperties","ISensor::SetProperties","SetProperties","SetProperties method","SetProperties method","ISensor interface","sensorsapi/ISensor::SetProperties","winsensors_com_ref.isensor_setproperties"]
old-location: winsensors_com_ref\isensor_setproperties.htm
tech.root: winsensors
ms.assetid: f2bed074-fcee-4dbb-a4c1-d5922d65d3b9
ms.date: 09/19/2025
ms.keywords: ISensor interface,SetProperties method, ISensor.SetProperties, ISensor::SetProperties, SetProperties, SetProperties method, SetProperties method,ISensor interface, sensorsapi/ISensor::SetProperties, winsensors_com_ref.isensor_setproperties
req.header: sensorsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
req.lib: Sensorsapi.lib
req.dll: Sensorsapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISensor::SetProperties
 - sensorsapi/ISensor::SetProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sensorsapi.dll
api_name:
 - ISensor.SetProperties
---

# ISensor::SetProperties


## -description

> [!IMPORTANT]
> Use the [UWP Sensor API](/windows/uwp/devices-sensors/sensors) instead.
>
> The COM-based Sensor API is deprecated and should not be used in new applications. No additional features or enhancements are planned, and support will be limited.

Specifies sensor properties.

## -parameters

### -param pProperties [in]

 Pointer to an <a href="/previous-versions//ms740012(v=vs.85)">IPortableDeviceValues</a> interface containing the list of properties and values to set.

### -param ppResults [out]

Address of an <b>IPortableDeviceValues</b> interface that receives the list of properties that were successfully set. Each property has an associated <b>HRESULT</b> value, which indicates whether setting the property succeeded.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The request to set one or more of the specified properties failed. Inspect <i>ppResults</i> to determine which properties, if any, succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL was passed in for ppResults.

</td>
</tr>
</table>

## -remarks

This method enables you to specify the values of one or more  properties, such as the sensor make, model, and serial number, by making a single call. 

Not all properties can be set.

<b>IPortableDeviceValues</b> is defined by the Windows Portable Devices API.


#### Examples

For an example of how to set properties, see <a href="/windows/desktop/SensorsAPI/setting-and-retrieving-sensor-properties">Setting and Retrieving Sensor Properties</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/sensorsapi/nf-sensorsapi-isensor-getproperties">GetProperties</a>



<a href="/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor">ISensor</a>