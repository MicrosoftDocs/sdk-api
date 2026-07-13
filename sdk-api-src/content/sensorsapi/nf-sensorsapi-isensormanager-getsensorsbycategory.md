---
UID: NF:sensorsapi.ISensorManager.GetSensorsByCategory
title: ISensorManager::GetSensorsByCategory (sensorsapi.h)
description: Retrieves a collection containing all sensors associated with the specified category.
helpviewer_keywords: ["GetSensorsByCategory","GetSensorsByCategory method","GetSensorsByCategory method","ISensorManager interface","ISensorManager interface","GetSensorsByCategory method","ISensorManager.GetSensorsByCategory","ISensorManager::GetSensorsByCategory","sensorsapi/ISensorManager::GetSensorsByCategory","winsensors_com_ref.isensormanager_getsensorsbycategory"]
old-location: winsensors_com_ref\isensormanager_getsensorsbycategory.htm
tech.root: winsensors
ms.assetid: 370e93ac-0854-4fe8-88d9-d23b80689c41
ms.date: 09/19/2025
ms.keywords: GetSensorsByCategory, GetSensorsByCategory method, GetSensorsByCategory method,ISensorManager interface, ISensorManager interface,GetSensorsByCategory method, ISensorManager.GetSensorsByCategory, ISensorManager::GetSensorsByCategory, sensorsapi/ISensorManager::GetSensorsByCategory, winsensors_com_ref.isensormanager_getsensorsbycategory
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
 - ISensorManager::GetSensorsByCategory
 - sensorsapi/ISensorManager::GetSensorsByCategory
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
 - ISensorManager.GetSensorsByCategory
---

# ISensorManager::GetSensorsByCategory


## -description

> [!IMPORTANT]
> Use the [UWP Sensor API](/windows/uwp/devices-sensors/sensors) instead.
>
> The COM-based Sensor API is deprecated and should not be used in new applications. No additional features or enhancements are planned, and support will be limited.

Retrieves a collection containing all sensors associated with the specified category.

## -parameters

### -param sensorCategory [in]

ID of the sensor category to retrieve.

### -param ppSensorsFound [out]

Address of an <a href="/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorcollection">ISensorCollection</a> interface pointer that receives a pointer to the sensor collection requested.

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
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)
</b></dt>
</dl>
</td>
<td width="60%">
No sensors are available for the specified category.

</td>
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