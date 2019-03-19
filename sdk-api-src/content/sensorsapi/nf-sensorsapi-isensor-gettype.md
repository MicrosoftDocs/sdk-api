---
UID: NF:sensorsapi.ISensor.GetType
title: ISensor::GetType (sensorsapi.h)
author: windows-sdk-content
description: Retrieves the sensor type ID.
old-location: winsensors_com_ref\isensor_gettype.htm
tech.root: SensorsAPI
ms.assetid: b01434ec-163a-4d91-a457-3d2a2c2a710a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetType, GetType method, GetType method,ISensor interface, ISensor interface,GetType method, ISensor.GetType, ISensor::GetType, sensorsapi/ISensor::GetType, winsensors_com_ref.isensor_gettype
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
 - ISensor.GetType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/3216afbb-d524-486d-99ad-0ee0cfb884e0">ISensor</a>



<a href="https://msdn.microsoft.com/38d87fb4-8f9f-412f-98e5-84651be2c759">Sensor Categories, Types, and Data Fields</a>
 

 

