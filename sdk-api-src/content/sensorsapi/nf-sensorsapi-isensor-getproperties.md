---
UID: NF:sensorsapi.ISensor.GetProperties
title: ISensor::GetProperties (sensorsapi.h)
description: Retrieves multiple sensor properties.
helpviewer_keywords: ["GetProperties","GetProperties method","GetProperties method","ISensor interface","ISensor interface","GetProperties method","ISensor.GetProperties","ISensor::GetProperties","sensorsapi/ISensor::GetProperties","winsensors_com_ref.isensor_getproperties"]
old-location: winsensors_com_ref\isensor_getproperties.htm
tech.root: winsensors
ms.assetid: 19581a45-500f-4210-9ec2-b3e33c84fb8a
ms.date: 09/19/2025
ms.keywords: GetProperties, GetProperties method, GetProperties method,ISensor interface, ISensor interface,GetProperties method, ISensor.GetProperties, ISensor::GetProperties, sensorsapi/ISensor::GetProperties, winsensors_com_ref.isensor_getproperties
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
 - ISensor::GetProperties
 - sensorsapi/ISensor::GetProperties
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
 - ISensor.GetProperties
---

# ISensor::GetProperties


## -description

> [!IMPORTANT]
> Use the [UWP Sensor API](/windows/uwp/devices-sensors/sensors) instead.
>
> The COM-based Sensor API is deprecated and should not be used in new applications. No additional features or enhancements are planned, and support will be limited.

Retrieves multiple sensor properties.

## -parameters

### -param pKeys [in]

Pointer to an <a href="/previous-versions//ms739549(v=vs.85)">IPortableDeviceKeyCollection</a> interface containing the <b>PROPERTYKEY</b> collection for the property values being requested. Set to <b>NULL</b> to retrieve all supported properties.

### -param ppProperties [out]

Address of an <a href="/previous-versions//ms740012(v=vs.85)">IPortableDeviceValues</a> pointer that receives the pointer to the requested property values.

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
The sensor driver does not support at least one of the specified properties. Each unsupported property <b>PROPVARIANT</b> returned through the <a href="/previous-versions//ms740012(v=vs.85)">IPortableDeviceValues</a> interface will have its error value set to <b>HRESULT_FROM_WIN32 
(ERROR_NOT_FOUND)</b>.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL was passed in for ppProperties.

</td>
</tr>
</table>

## -remarks

This method enables you to retrieve the values of multiple properties, such as the sensor make, model, and serial number, by making a single call. To retrieve a single property, call <a href="/windows/desktop/api/sensorsapi/nf-sensorsapi-isensor-getproperty">ISensor::GetProperty</a>.

The <b>IPortableDeviceKeyCollection</b> and <b>IPortableDeviceValues</b> interfaces are defined by the Windows Portable Devices API. 


#### Examples

For an example of how to retrieve properties from a sensor,  see <a href="/windows/desktop/SensorsAPI/setting-and-retrieving-sensor-properties">Setting and Retrieving Sensor Properties</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor">ISensor</a>



<a href="/windows/desktop/SensorsAPI/sensor-properties">Sensor Properties</a>



<a href="/windows/desktop/api/sensorsapi/nf-sensorsapi-isensor-setproperties">SetProperties</a>