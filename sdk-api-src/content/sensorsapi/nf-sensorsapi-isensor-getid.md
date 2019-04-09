---
UID: NF:sensorsapi.ISensor.GetID
title: ISensor::GetID (sensorsapi.h)
author: windows-sdk-content
description: Retrieves the unique identifier of the sensor.
old-location: winsensors_com_ref\isensor_getid.htm
tech.root: SensorsAPI
ms.assetid: f314060d-ed39-48b1-b8b1-8659c05be549
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetID, GetID method, GetID method,ISensor interface, ISensor interface,GetID method, ISensor.GetID, ISensor::GetID, sensorsapi/ISensor::GetID, winsensors_com_ref.isensor_getid
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
 - ISensor.GetID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISensor::GetID


## -description


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

You can use an ID to retrieve a pointer to a particular sensor by calling <a href="https://msdn.microsoft.com/453f46f3-43e1-466d-9f46-165b7d2bcd56">ISensorManager::GetSensorByID</a>.





## -see-also




<a href="https://msdn.microsoft.com/3216afbb-d524-486d-99ad-0ee0cfb884e0">ISensor</a>



<a href="https://msdn.microsoft.com/ba85ccd8-5251-4e47-84da-80899fe84c39">Sensor Constants</a>
 

 

