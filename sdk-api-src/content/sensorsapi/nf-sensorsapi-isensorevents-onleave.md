---
UID: NF:sensorsapi.ISensorEvents.OnLeave
title: ISensorEvents::OnLeave (sensorsapi.h)
description: Provides notification that a sensor device is no longer connected.
helpviewer_keywords: ["ISensorEvents interface","OnLeave method","ISensorEvents.OnLeave","ISensorEvents::OnLeave","OnLeave","OnLeave method","OnLeave method","ISensorEvents interface","sensorsapi/ISensorEvents::OnLeave","winsensors_com_ref.isensorevents_onleave"]
old-location: winsensors_com_ref\isensorevents_onleave.htm
tech.root: winsensors
ms.assetid: 541ef7a4-c238-4fc5-9b2d-1fadb1472b2d
ms.date: 09/19/2025
ms.keywords: ISensorEvents interface,OnLeave method, ISensorEvents.OnLeave, ISensorEvents::OnLeave, OnLeave, OnLeave method, OnLeave method,ISensorEvents interface, sensorsapi/ISensorEvents::OnLeave, winsensors_com_ref.isensorevents_onleave
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
 - ISensorEvents::OnLeave
 - sensorsapi/ISensorEvents::OnLeave
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
 - ISensorEvents.OnLeave
---

# ISensorEvents::OnLeave


## -description

> [!IMPORTANT]
> Use the [UWP Sensor API](/windows/uwp/devices-sensors/sensors) instead.
>
> The COM-based Sensor API is deprecated and should not be used in new applications. No additional features or enhancements are planned, and support will be limited.

Provides notification that a sensor device is no longer connected.

## -parameters

### -param ID [in]

The ID of the sensor.

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

To know when a sensor enters, subscribe to the <a href="/windows/desktop/api/sensorsapi/nf-sensorsapi-isensormanagerevents-onsensorenter">ISensorManagerEvents::OnSensorEnter</a> event.


#### Examples

For an example of how to receive sensor events, see <a href="/windows/desktop/SensorsAPI/using-sensor-api-events">Using Sensor API Events</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents">ISensorEvents</a>