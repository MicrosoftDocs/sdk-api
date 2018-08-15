---
UID: NF:sensorsapi.ISensor.GetCategory
title: ISensor::GetCategory
author: windows-sdk-content
description: Retrieves the identifier of the sensor category.
old-location: winsensors_com_ref\isensor_getcategory.htm
old-project: SensorsAPI
ms.assetid: 3a4eab1c-ec6f-4d6e-8479-1fa7f87537f7
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetCategory, GetCategory method, GetCategory method,ISensor interface, ISensor interface,GetCategory method, ISensor.GetCategory, ISensor::GetCategory, sensorsapi/ISensor::GetCategory, winsensors_com_ref.isensor_getcategory
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: sensorsapi.h
req.include-header: 
req.redist: 
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
 - ISensor.GetCategory
product: Windows
targetos: Windows
req.lib: Sensorsapi.lib
req.dll: Sensorsapi.dll
req.irql: 
req.product: ADAM
---

# ISensor::GetCategory


## -description


Retrieves the identifier of the sensor category.


## -parameters




### -param pSensorCategory [out]

Address of a <b>SENSOR_CATEGORY_ID</b> that receives the sensor category ID.


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
The sensor driver did not provide a category value. The <b>PROPVARIANT</b> returned will have its error value set to <b>HRESULT_FROM_WIN32 
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
NULL was passed in for pSensorCategory.

</td>
</tr>
</table>
 




## -remarks



A <b>SENSOR_CATEGORY_ID</b> is a <b>GUID</b> that uniquely identifies the sensor category.




## -see-also




<a href="https://msdn.microsoft.com/3216afbb-d524-486d-99ad-0ee0cfb884e0">ISensor</a>



<a href="https://msdn.microsoft.com/38d87fb4-8f9f-412f-98e5-84651be2c759">Sensor Categories, Types, and Data Fields</a>
 

 

