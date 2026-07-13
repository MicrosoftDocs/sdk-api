---
UID: NF:sensorsapi.ISensor.GetState
title: ISensor::GetState (sensorsapi.h)
description: Retrieves the current operational state of the sensor.
helpviewer_keywords: ["GetState","GetState method","GetState method","ISensor interface","ISensor interface","GetState method","ISensor.GetState","ISensor::GetState","sensorsapi/ISensor::GetState","winsensors_com_ref.isensor_getstate"]
old-location: winsensors_com_ref\isensor_getstate.htm
tech.root: winsensors
ms.assetid: ec8683a5-f2b3-48ce-8732-16429ee16a7f
ms.date: 09/19/2025
ms.keywords: GetState, GetState method, GetState method,ISensor interface, ISensor interface,GetState method, ISensor.GetState, ISensor::GetState, sensorsapi/ISensor::GetState, winsensors_com_ref.isensor_getstate
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
 - ISensor::GetState
 - sensorsapi/ISensor::GetState
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
 - ISensor.GetState
---

# ISensor::GetState


## -description

> [!IMPORTANT]
> Use the [UWP Sensor API](/windows/uwp/devices-sensors/sensors) instead.
>
> The COM-based Sensor API is deprecated and should not be used in new applications. No additional features or enhancements are planned, and support will be limited.

Retrieves the current operational state of the sensor.

## -parameters

### -param pState [out]

Address of a <a href="/windows/win32/api/sensorsapi/ne-sensorsapi-sensorstate">SensorState</a> variable that receives the current state.

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
The sensor driver did not provide a state value. The value provided through <i>pState</i> is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL was passed in for pState.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor">ISensor</a>