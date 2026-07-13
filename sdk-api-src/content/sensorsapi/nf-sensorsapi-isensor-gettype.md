---
UID: NF:sensorsapi.ISensor.GetType
title: ISensor::GetType (sensorsapi.h)
description: Retrieves the sensor type ID.
helpviewer_keywords: ["GetType","GetType method","GetType method","ISensor interface","ISensor interface","GetType method","ISensor.GetType","ISensor::GetType","sensorsapi/ISensor::GetType","winsensors_com_ref.isensor_gettype"]
old-location: winsensors_com_ref\isensor_gettype.htm
tech.root: winsensors
ms.assetid: b01434ec-163a-4d91-a457-3d2a2c2a710a
ms.date: 09/19/2025
ms.keywords: GetType, GetType method, GetType method,ISensor interface, ISensor interface,GetType method, ISensor.GetType, ISensor::GetType, sensorsapi/ISensor::GetType, winsensors_com_ref.isensor_gettype
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
 - ISensor::GetType
 - sensorsapi/ISensor::GetType
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
 - ISensor.GetType
---

# ISensor::GetType


## -description

> [!IMPORTANT]
> Use the [UWP Sensor API](/windows/uwp/devices-sensors/sensors) instead.
>
> The COM-based Sensor API is deprecated and should not be used in new applications. No additional features or enhancements are planned, and support will be limited.

Retrieves the sensor type ID.

## -parameters

### -param pSensorType [out]

Address of a <b>SENSOR_TYPE_ID</b> that receives the sensor type ID.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The sensor driver did not provide a sensor type value. The <b>PROPVARIANT</b> returned will have its error value set to <b>HRESULT_FROM_WIN32 
( ERROR_NOT_FOUND)</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL was passed in for pSensorType.

</td>
</tr>
</table>

## -remarks

Sensor types are more specific groupings than sensor categories.
Sensor type IDs are <b>GUID</b>s that are defined in Sensors.h.

## -see-also

<a href="/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor">ISensor</a>



<a href="/windows/desktop/SensorsAPI/sensor-categories--types--and-datafields">Sensor Categories, Types, and Data Fields</a>