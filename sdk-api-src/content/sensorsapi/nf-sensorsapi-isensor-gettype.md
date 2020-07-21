---
UID: NF:sensorsapi.ISensor.GetType
title: ISensor::GetType (sensorsapi.h)
description: Retrieves the sensor type ID.
helpviewer_keywords: ["GetType","GetType method","GetType method","ISensor interface","ISensor interface","GetType method","ISensor.GetType","ISensor::GetType","sensorsapi/ISensor::GetType","winsensors_com_ref.isensor_gettype"]
old-location: winsensors_com_ref\isensor_gettype.htm
tech.root: SensorsAPI
ms.assetid: b01434ec-163a-4d91-a457-3d2a2c2a710a
ms.date: 12/05/2018
ms.keywords: GetType, GetType method, GetType method,ISensor interface, ISensor interface,GetType method, ISensor.GetType, ISensor::GetType, sensorsapi/ISensor::GetType, winsensors_com_ref.isensor_gettype
f1_keywords:
- sensorsapi/ISensor.GetType
dev_langs:
- c++
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
- ISensor.GetType
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISensor::GetType


## -description


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




<a href="https://docs.microsoft.com/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor">ISensor</a>



<a href="https://docs.microsoft.com/windows/desktop/SensorsAPI/sensor-categories--types--and-datafields">Sensor Categories, Types, and Data Fields</a>
 

 

