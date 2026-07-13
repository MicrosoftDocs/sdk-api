---
UID: NF:sensorsapi.ISensorManagerEvents.OnSensorEnter
title: ISensorManagerEvents::OnSensorEnter (sensorsapi.h)
description: Provides notification when a sensor device is connected.
helpviewer_keywords: ["ISensorManagerEvents interface","OnSensorEnter method","ISensorManagerEvents.OnSensorEnter","ISensorManagerEvents::OnSensorEnter","OnSensorEnter","OnSensorEnter method","OnSensorEnter method","ISensorManagerEvents interface","sensorsapi/ISensorManagerEvents::OnSensorEnter","winsensors_com_ref.isensormanagerevents_onsensorenter","winsensors_com_ref.isensormanagerevents_sensorenter"]
old-location: winsensors_com_ref\isensormanagerevents_onsensorenter.htm
tech.root: winsensors
ms.assetid: 1316e3b0-9677-4575-a3b8-53fa57295987
ms.date: 09/19/2025
ms.keywords: ISensorManagerEvents interface,OnSensorEnter method, ISensorManagerEvents.OnSensorEnter, ISensorManagerEvents::OnSensorEnter, OnSensorEnter, OnSensorEnter method, OnSensorEnter method,ISensorManagerEvents interface, sensorsapi/ISensorManagerEvents::OnSensorEnter, winsensors_com_ref.isensormanagerevents_onsensorenter, winsensors_com_ref.isensormanagerevents_sensorenter
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
 - ISensorManagerEvents::OnSensorEnter
 - sensorsapi/ISensorManagerEvents::OnSensorEnter
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
 - ISensorManagerEvents.OnSensorEnter
---

# ISensorManagerEvents::OnSensorEnter


## -description

> [!IMPORTANT]
> Use the [UWP Sensor API](/windows/uwp/devices-sensors/sensors) instead.
>
> The COM-based Sensor API is deprecated and should not be used in new applications. No additional features or enhancements are planned, and support will be limited.

Provides notification when a sensor device is connected.

## -parameters

### -param pSensor [in]

A pointer to the <a href="/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor">ISensor</a> interface of the sensor that was connected.

### -param state [in]

<a href="/windows/win32/api/sensorsapi/ne-sensorsapi-sensorstate">SensorState</a> indicating the current state of the sensor.

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
</table>

## -remarks

To know when a sensor is disconnected, subscribe to the <a href="/windows/desktop/api/sensorsapi/nf-sensorsapi-isensorevents-onleave">ISensorEvents::OnLeave</a> event.

## -see-also

<a href="/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanagerevents">ISensorManagerEvents</a>