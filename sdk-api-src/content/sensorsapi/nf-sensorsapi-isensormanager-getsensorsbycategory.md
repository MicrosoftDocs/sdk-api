---
UID: NF:sensorsapi.ISensorManager.GetSensorsByCategory
title: ISensorManager::GetSensorsByCategory
author: windows-sdk-content
description: Retrieves a collection containing all sensors associated with the specified category.
old-location: winsensors_com_ref\isensormanager_getsensorsbycategory.htm
tech.root: SensorsAPI
ms.assetid: 370e93ac-0854-4fe8-88d9-d23b80689c41
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetSensorsByCategory, GetSensorsByCategory method, GetSensorsByCategory method,ISensorManager interface, ISensorManager interface,GetSensorsByCategory method, ISensorManager.GetSensorsByCategory, ISensorManager::GetSensorsByCategory, sensorsapi/ISensorManager::GetSensorsByCategory, winsensors_com_ref.isensormanager_getsensorsbycategory
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ISensorManager.GetSensorsByCategory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISensorManager::GetSensorsByCategory


## -description


Retrieves a collection containing all sensors associated with the specified category.


## -parameters




### -param sensorCategory [in]

ID of the sensor category to retrieve.


### -param ppSensorsFound [out]

Address of an <a href="https://msdn.microsoft.com/54d8572a-40a2-49d0-a8bf-2161b63eee42">ISensorCollection</a> interface pointer that receives a pointer to the sensor collection requested.


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




<a href="https://msdn.microsoft.com/313742c9-58a7-4ddd-9582-a6ee276e97d0">ISensorManager</a>



<a href="https://msdn.microsoft.com/36631bae-f237-4951-9959-6ab6286bd1f7">Retrieving a Sensor Object</a>
 

 

