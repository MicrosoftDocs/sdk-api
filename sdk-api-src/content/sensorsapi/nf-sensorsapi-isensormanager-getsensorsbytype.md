---
UID: NF:sensorsapi.ISensorManager.GetSensorsByType
title: ISensorManager::GetSensorsByType
author: windows-sdk-content
description: Retrieves a collection containing all sensors associated with the specified type.
old-location: winsensors_com_ref\isensormanager_getsensorsbytype.htm
old-project: SensorsAPI
ms.assetid: f383d7e3-bcd0-457d-a410-9ac225f1d147
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: GetSensorsByType, GetSensorsByType method, GetSensorsByType method,ISensorManager interface, ISensorManager interface,GetSensorsByType method, ISensorManager.GetSensorsByType, ISensorManager::GetSensorsByType, sensorsapi/ISensorManager::GetSensorsByType, winsensors_com_ref.isensormanager_getsensorsbytype
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: SensorConnectionType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sensorsapi.dll
api_name:
 - ISensorManager.GetSensorsByType
product: Windows
targetos: Windows
req.lib: Sensorsapi.lib
req.dll: Sensorsapi.dll
req.irql: 
req.product: ADAM
---

# ISensorManager::GetSensorsByType


## -description


Retrieves a collection containing all sensors associated with the specified type.


## -parameters




### -param sensorType [in]

ID of the type of sensors to retrieve.


### -param ppSensorsFound [out]

Address of an <a href="https://msdn.microsoft.com/54d8572a-40a2-49d0-a8bf-2161b63eee42">ISensorCollection</a> interface pointer that receives the pointer to the sensor collection requested.


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




<a href="https://msdn.microsoft.com/313742c9-58a7-4ddd-9582-a6ee276e97d0">ISensorManager</a>



<a href="https://msdn.microsoft.com/36631bae-f237-4951-9959-6ab6286bd1f7">Retrieving a Sensor Object</a>
 

 

