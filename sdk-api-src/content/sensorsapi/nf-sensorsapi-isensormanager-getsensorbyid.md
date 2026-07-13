---
UID: NF:sensorsapi.ISensorManager.GetSensorByID
title: ISensorManager::GetSensorByID (sensorsapi.h)
description: Retrieves a pointer to the specified sensor.
helpviewer_keywords: ["GetSensorByID","GetSensorByID method","GetSensorByID method","ISensorManager interface","ISensorManager interface","GetSensorByID method","ISensorManager.GetSensorByID","ISensorManager::GetSensorByID","sensorsapi/ISensorManager::GetSensorByID","winsensors_com_ref.isensormanager_getsensorbyid"]
old-location: winsensors_com_ref\isensormanager_getsensorbyid.htm
tech.root: winsensors
ms.assetid: 453f46f3-43e1-466d-9f46-165b7d2bcd56
ms.date: 09/19/2025
ms.keywords: GetSensorByID, GetSensorByID method, GetSensorByID method,ISensorManager interface, ISensorManager interface,GetSensorByID method, ISensorManager.GetSensorByID, ISensorManager::GetSensorByID, sensorsapi/ISensorManager::GetSensorByID, winsensors_com_ref.isensormanager_getsensorbyid
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
 - ISensorManager::GetSensorByID
 - sensorsapi/ISensorManager::GetSensorByID
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
 - ISensorManager.GetSensorByID
---

# ISensorManager::GetSensorByID


## -description

> [!IMPORTANT]
> Use the [UWP Sensor API](/windows/uwp/devices-sensors/sensors) instead.
>
> The COM-based Sensor API is deprecated and should not be used in new applications. No additional features or enhancements are planned, and support will be limited.

Retrieves a pointer to the specified sensor.

## -parameters

### -param sensorID [in]

The ID of the sensor to retrieve.

### -param ppSensor [out]

Address of an <a href="/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor">ISensor</a> interface pointer that receives a pointer to the requested sensor. Will be <b>NULL</b> if the requested sensor cannot be found.

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
The sensor manager found more than one sensor with the same ID.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)
</b></dt>
</dl>
</td>
<td width="60%">
No sensor is available for the specified ID.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL was passed in for ppSensor.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager">ISensorManager</a>



<a href="/windows/desktop/SensorsAPI/retrieving-a-sensor">Retrieving a Sensor Object</a>