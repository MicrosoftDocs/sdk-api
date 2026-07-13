---
UID: NF:sensorsapi.ISensor.SetEventSink
title: ISensor::SetEventSink (sensorsapi.h)
description: Specifies the interface through which to receive sensor event notifications.
helpviewer_keywords: ["ISensor interface","SetEventSink method","ISensor.SetEventSink","ISensor::SetEventSink","SetEventSink","SetEventSink method","SetEventSink method","ISensor interface","sensorsapi/ISensor::SetEventSink","winsensors_com_ref.isensor_seteventsink"]
old-location: winsensors_com_ref\isensor_seteventsink.htm
tech.root: winsensors
ms.assetid: 8e2f7edc-894f-4258-8948-2a3d4df532c3
ms.date: 09/19/2025
ms.keywords: ISensor interface,SetEventSink method, ISensor.SetEventSink, ISensor::SetEventSink, SetEventSink, SetEventSink method, SetEventSink method,ISensor interface, sensorsapi/ISensor::SetEventSink, winsensors_com_ref.isensor_seteventsink
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
 - ISensor::SetEventSink
 - sensorsapi/ISensor::SetEventSink
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
 - ISensor.SetEventSink
---

# ISensor::SetEventSink


## -description

> [!IMPORTANT]
> Use the [UWP Sensor API](/windows/uwp/devices-sensors/sensors) instead.
>
> The COM-based Sensor API is deprecated and should not be used in new applications. No additional features or enhancements are planned, and support will be limited.

Specifies the interface through which to receive sensor event notifications.

## -parameters

### -param pEvents [in]

Pointer to the <a href="/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents">ISensorEvents</a> callback interface that receives the event notifications. Set to <b>NULL</b> to cancel event notifications.

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

Specify the events to receive by calling <a href="/windows/desktop/api/sensorsapi/nf-sensorsapi-isensor-seteventinterest">SetEventInterest</a>. You can retrieve the current event interest list by calling <a href="/windows/desktop/api/sensorsapi/nf-sensorsapi-isensor-geteventinterest">GetEventInterest</a>.


#### Examples

For an example of how to set the event sink, see <a href="/windows/desktop/SensorsAPI/using-sensor-api-events">Using Sensor API Events</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor">ISensor</a>