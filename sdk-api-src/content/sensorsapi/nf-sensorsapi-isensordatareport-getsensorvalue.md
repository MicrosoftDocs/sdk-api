---
UID: NF:sensorsapi.ISensorDataReport.GetSensorValue
title: ISensorDataReport::GetSensorValue (sensorsapi.h)
description: Retrieves a single data field value from the data report.
helpviewer_keywords: ["GetSensorValue","GetSensorValue method","GetSensorValue method","ISensorDataReport interface","ISensorDataReport interface","GetSensorValue method","ISensorDataReport.GetSensorValue","ISensorDataReport::GetSensorValue","sensorsapi/ISensorDataReport::GetSensorValue","winsensors_com_ref.isensordatareport_getsensorvalue"]
old-location: winsensors_com_ref\isensordatareport_getsensorvalue.htm
tech.root: winsensors
ms.assetid: cd4aab72-558c-4f56-a9c1-b10213823c28
ms.date: 09/19/2025
ms.keywords: GetSensorValue, GetSensorValue method, GetSensorValue method,ISensorDataReport interface, ISensorDataReport interface,GetSensorValue method, ISensorDataReport.GetSensorValue, ISensorDataReport::GetSensorValue, sensorsapi/ISensorDataReport::GetSensorValue, winsensors_com_ref.isensordatareport_getsensorvalue
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
 - ISensorDataReport::GetSensorValue
 - sensorsapi/ISensorDataReport::GetSensorValue
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
 - ISensorDataReport.GetSensorValue
---

# ISensorDataReport::GetSensorValue


## -description

> [!IMPORTANT]
> Use the [UWP Sensor API](/windows/uwp/devices-sensors/sensors) instead.
>
> The COM-based Sensor API is deprecated and should not be used in new applications. No additional features or enhancements are planned, and support will be limited.

Retrieves a single data field value from the data report.

## -parameters

### -param pKey [in]

<b>REFPROPERTYKEY</b> indicating the data field to retrieve.

### -param pValue [out]

Address of a <b>PROPVARIANT</b> that receives the data field value.

## -returns

This method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The data field was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL was passed in for pValue.

</td>
</tr>
</table>

## -remarks

Platform-defined data field <b>PROPERTYKEY</b>s are defined in Sensors.h.


#### Examples

For an example of how to retrieve a sensor data field value, see <a href="/windows/desktop/SensorsAPI/retrieving-sensor-data-fields">Retrieving Sensor Data Values</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport">ISensorDataReport</a>