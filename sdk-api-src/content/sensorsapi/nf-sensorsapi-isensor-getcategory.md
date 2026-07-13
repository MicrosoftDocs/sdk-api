---
UID: NF:sensorsapi.ISensor.GetCategory
title: ISensor::GetCategory (sensorsapi.h)
description: Retrieves the identifier of the sensor category.
helpviewer_keywords: ["GetCategory","GetCategory method","GetCategory method","ISensor interface","ISensor interface","GetCategory method","ISensor.GetCategory","ISensor::GetCategory","sensorsapi/ISensor::GetCategory","winsensors_com_ref.isensor_getcategory"]
old-location: winsensors_com_ref\isensor_getcategory.htm
tech.root: winsensors
ms.assetid: 3a4eab1c-ec6f-4d6e-8479-1fa7f87537f7
ms.date: 09/19/2025
ms.keywords: GetCategory, GetCategory method, GetCategory method,ISensor interface, ISensor interface,GetCategory method, ISensor.GetCategory, ISensor::GetCategory, sensorsapi/ISensor::GetCategory, winsensors_com_ref.isensor_getcategory
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
 - ISensor::GetCategory
 - sensorsapi/ISensor::GetCategory
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
 - ISensor.GetCategory
---

# ISensor::GetCategory


## -description

> [!IMPORTANT]
> Use the [UWP Sensor API](/windows/uwp/devices-sensors/sensors) instead.
>
> The COM-based Sensor API is deprecated and should not be used in new applications. No additional features or enhancements are planned, and support will be limited.

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

<a href="/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor">ISensor</a>



<a href="/windows/desktop/SensorsAPI/sensor-categories--types--and-datafields">Sensor Categories, Types, and Data Fields</a>