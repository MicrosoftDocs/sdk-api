---
UID: NF:sensorsapi.ISensor.GetData
title: ISensor::GetData
author: windows-sdk-content
description: Retrieves the most recent sensor data report.
old-location: winsensors_com_ref\isensor_getdata.htm
tech.root: SensorsAPI
ms.assetid: 89145856-96c7-48c2-988c-b410ab20aed4
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetData, GetData method, GetData method,ISensor interface, ISensor interface,GetData method, ISensor.GetData, ISensor::GetData, sensorsapi/ISensor::GetData, winsensors_com_ref.isensor_getdata
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
 - ISensor.GetData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISensor::GetData


## -description


Retrieves the most recent sensor data report.


## -parameters




### -param ppDataReport [out]

Address of an <a href="https://msdn.microsoft.com/c677b956-e3ab-477c-b97b-aceec4e2d235">ISensorDataReport</a> pointer that receives the pointer to the most recent sensor data report.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The sensor driver provided badly formed data. For example, the data was of a type that is not supported. For information about data types of platform-defined data fields, see <a href="https://msdn.microsoft.com/38d87fb4-8f9f-412f-98e5-84651be2c759">Sensor Categories, Types, and Data Fields</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NO_DATA)</b></dt>
</dl>
</td>
<td width="60%">
The sensor has no data to report. For example, a GPS sensor could be in the process of acquiring a satellite fix.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL was passed in for ppDataReport.

</td>
</tr>
</table>
 




## -remarks



For location sensors, you can retrieve data only from sensors for which the user has granted permission.

This method may return data before the driver has set the state to SENSOR_STATE_READY.


#### Examples

For an example of how to retrieve sensor data, see <a href="https://msdn.microsoft.com/4ae80816-5e53-4ed1-9300-4b38c22d65e2">Retrieving Sensor Data Values</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/3216afbb-d524-486d-99ad-0ee0cfb884e0">ISensor</a>



<a href="https://msdn.microsoft.com/c755edcf-18c1-43d5-9dfe-c073e1f96b5f">Managing User Permissions</a>



<a href="https://msdn.microsoft.com/6a21820c-4f13-4220-ad13-34d0226597b6">RequestPermissions</a>



<a href="https://msdn.microsoft.com/38d87fb4-8f9f-412f-98e5-84651be2c759">Sensor Categories, Types, and Data Fields</a>
 

 

