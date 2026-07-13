---
UID: NF:sensorsapi.ISensor.GetData
title: ISensor::GetData (sensorsapi.h)
description: Retrieves the most recent sensor data report.
helpviewer_keywords: ["GetData","GetData method","GetData method","ISensor interface","ISensor interface","GetData method","ISensor.GetData","ISensor::GetData","sensorsapi/ISensor::GetData","winsensors_com_ref.isensor_getdata"]
old-location: winsensors_com_ref\isensor_getdata.htm
tech.root: winsensors
ms.assetid: 89145856-96c7-48c2-988c-b410ab20aed4
ms.date: 09/19/2025
ms.keywords: GetData, GetData method, GetData method,ISensor interface, ISensor interface,GetData method, ISensor.GetData, ISensor::GetData, sensorsapi/ISensor::GetData, winsensors_com_ref.isensor_getdata
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
 - ISensor::GetData
 - sensorsapi/ISensor::GetData
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
 - ISensor.GetData
---

# ISensor::GetData


## -description

> [!IMPORTANT]
> Use the [UWP Sensor API](/windows/uwp/devices-sensors/sensors) instead.
>
> The COM-based Sensor API is deprecated and should not be used in new applications. No additional features or enhancements are planned, and support will be limited.

Retrieves the most recent sensor data report.

## -parameters

### -param ppDataReport [out]

Address of an <a href="/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport">ISensorDataReport</a> pointer that receives the pointer to the most recent sensor data report.

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
The sensor driver provided badly formed data. For example, the data was of a type that is not supported. For information about data types of platform-defined data fields, see <a href="/windows/desktop/SensorsAPI/sensor-categories--types--and-datafields">Sensor Categories, Types, and Data Fields</a>.

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

For an example of how to retrieve sensor data, see <a href="/windows/desktop/SensorsAPI/retrieving-sensor-data-fields">Retrieving Sensor Data Values</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor">ISensor</a>



<a href="/windows/desktop/SensorsAPI/managing-user-permissions">Managing User Permissions</a>



<a href="/windows/desktop/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions">RequestPermissions</a>



<a href="/windows/desktop/SensorsAPI/sensor-categories--types--and-datafields">Sensor Categories, Types, and Data Fields</a>