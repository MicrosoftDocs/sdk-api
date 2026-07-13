---
UID: NF:sensorsapi.ISensorManager.GetSensorsByType
title: ISensorManager::GetSensorsByType (sensorsapi.h)
description: Retrieves a collection containing all sensors associated with the specified type.
helpviewer_keywords: ["GetSensorsByType","GetSensorsByType method","GetSensorsByType method","ISensorManager interface","ISensorManager interface","GetSensorsByType method","ISensorManager.GetSensorsByType","ISensorManager::GetSensorsByType","sensorsapi/ISensorManager::GetSensorsByType","winsensors_com_ref.isensormanager_getsensorsbytype"]
old-location: winsensors_com_ref\isensormanager_getsensorsbytype.htm
tech.root: winsensors
ms.assetid: f383d7e3-bcd0-457d-a410-9ac225f1d147
ms.date: 09/19/2025
ms.keywords: GetSensorsByType, GetSensorsByType method, GetSensorsByType method,ISensorManager interface, ISensorManager interface,GetSensorsByType method, ISensorManager.GetSensorsByType, ISensorManager::GetSensorsByType, sensorsapi/ISensorManager::GetSensorsByType, winsensors_com_ref.isensormanager_getsensorsbytype
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
 - ISensorManager::GetSensorsByType
 - sensorsapi/ISensorManager::GetSensorsByType
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
 - ISensorManager.GetSensorsByType
---

# ISensorManager::GetSensorsByType


## -description

> [!IMPORTANT]
> Use the [UWP Sensor API](/windows/uwp/devices-sensors/sensors) instead.
>
> The COM-based Sensor API is deprecated and should not be used in new applications. No additional features or enhancements are planned, and support will be limited.

Retrieves a collection containing all sensors associated with the specified type.

## -parameters

### -param sensorType [in]

ID of the type of sensors to retrieve.

### -param ppSensorsFound [out]

Address of an <a href="/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorcollection">ISensorCollection</a> interface pointer that receives the pointer to the sensor collection requested.

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
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)
</b></dt>
</dl>
</td>
<td width="60%">
No sensors are available for the specified type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL was passed in for ppSensorsFound.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager">ISensorManager</a>



<a href="/windows/desktop/SensorsAPI/retrieving-a-sensor">Retrieving a Sensor Object</a>