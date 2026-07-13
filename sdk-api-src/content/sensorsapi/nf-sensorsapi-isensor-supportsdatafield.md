---
UID: NF:sensorsapi.ISensor.SupportsDataField
title: ISensor::SupportsDataField (sensorsapi.h)
description: Indicates whether the sensor supports the specified data field.
helpviewer_keywords: ["ISensor interface","SupportsDataField method","ISensor.SupportsDataField","ISensor::SupportsDataField","SupportsDataField","SupportsDataField method","SupportsDataField method","ISensor interface","sensorsapi/ISensor::SupportsDataField","winsensors_com_ref.isensor_supportsdatafield"]
old-location: winsensors_com_ref\isensor_supportsdatafield.htm
tech.root: winsensors
ms.assetid: 95e7211f-9335-4ecf-b9e9-b86ec6a63cba
ms.date: 09/19/2025
ms.keywords: ISensor interface,SupportsDataField method, ISensor.SupportsDataField, ISensor::SupportsDataField, SupportsDataField, SupportsDataField method, SupportsDataField method,ISensor interface, sensorsapi/ISensor::SupportsDataField, winsensors_com_ref.isensor_supportsdatafield
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
 - ISensor::SupportsDataField
 - sensorsapi/ISensor::SupportsDataField
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
 - ISensor.SupportsDataField
---

# ISensor::SupportsDataField


## -description

> [!IMPORTANT]
> Use the [UWP Sensor API](/windows/uwp/devices-sensors/sensors) instead.
>
> The COM-based Sensor API is deprecated and should not be used in new applications. No additional features or enhancements are planned, and support will be limited.

Indicates whether the sensor supports the specified data field.

## -parameters

### -param key [in]

<b>REFPROPERTYKEY</b> value specifying the data field to search for.

### -param pIsSupported [out]

Address of a <b>VARIANT_BOOL</b> that receives a value indicating whether the sensor supports the data field.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL was passed in for pIsSupported.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor">ISensor</a>