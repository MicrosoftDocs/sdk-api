---
UID: NF:sensorsapi.ISensorManager.GetSensorByID
title: ISensorManager::GetSensorByID (sensorsapi.h)
author: windows-sdk-content
description: Retrieves a pointer to the specified sensor.
old-location: winsensors_com_ref\isensormanager_getsensorbyid.htm
tech.root: SensorsAPI
ms.assetid: 453f46f3-43e1-466d-9f46-165b7d2bcd56
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetSensorByID, GetSensorByID method, GetSensorByID method,ISensorManager interface, ISensorManager interface,GetSensorByID method, ISensorManager.GetSensorByID, ISensorManager::GetSensorByID, sensorsapi/ISensorManager::GetSensorByID, winsensors_com_ref.isensormanager_getsensorbyid
ms.topic: method
f1_keywords: 
 - "sensorsapi/ISensorManager.GetSensorByID"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sensorsapi.dll
api_name:
 - ISensorManager.GetSensorByID
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISensorManager::GetSensorByID


## -description


Retrieves a pointer to the specified sensor.


## -parameters




### -param sensorID [in]

The ID of the sensor to retrieve.


### -param ppSensor [out]

Address of an <a href="https://docs.microsoft.com/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor">ISensor</a> interface pointer that receives a pointer to the requested sensor. Will be <b>NULL</b> if the requested sensor cannot be found.


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




<a href="https://docs.microsoft.com/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager">ISensorManager</a>



<a href="https://docs.microsoft.com/windows/desktop/SensorsAPI/retrieving-a-sensor">Retrieving a Sensor Object</a>
 

 

