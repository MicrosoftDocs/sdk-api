---
UID: NF:sensorsapi.ISensor.GetID
title: ISensor::GetID (sensorsapi.h)
description: Retrieves the unique identifier of the sensor.
helpviewer_keywords: ["GetID","GetID method","GetID method","ISensor interface","ISensor interface","GetID method","ISensor.GetID","ISensor::GetID","sensorsapi/ISensor::GetID","winsensors_com_ref.isensor_getid"]
old-location: winsensors_com_ref\isensor_getid.htm
tech.root: winsensors
ms.assetid: f314060d-ed39-48b1-b8b1-8659c05be549
ms.date: 09/19/2025
ms.keywords: GetID, GetID method, GetID method,ISensor interface, ISensor interface,GetID method, ISensor.GetID, ISensor::GetID, sensorsapi/ISensor::GetID, winsensors_com_ref.isensor_getid
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
 - ISensor::GetID
 - sensorsapi/ISensor::GetID
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
 - ISensor.GetID
---

# ISensor::GetID


## -description

> [!IMPORTANT]
> Use the [UWP Sensor API](/windows/uwp/devices-sensors/sensors) instead.
>
> The COM-based Sensor API is deprecated and should not be used in new applications. No additional features or enhancements are planned, and support will be limited.

Retrieves the unique identifier of the sensor.

## -parameters

### -param pID [out]

Address of a <b>SENSOR_ID</b> that receives the ID.

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
The sensor driver did not provide a sensor ID.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL was passed in for pID.

</td>
</tr>
</table>

## -remarks

A <b>SENSOR_ID</b> is a <b>GUID</b> that uniquely identifies the sensor on the current computer. This ID corresponds to the constant named SENSOR_PROPERTY_PERSISTENT_UNIQUE_ID.

You can use an ID to retrieve a pointer to a particular sensor by calling <a href="/windows/desktop/api/sensorsapi/nf-sensorsapi-isensormanager-getsensorbyid">ISensorManager::GetSensorByID</a>.

## -see-also

<a href="/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor">ISensor</a>



<a href="/windows/desktop/SensorsAPI/about-sensor-constants">Sensor Constants</a>