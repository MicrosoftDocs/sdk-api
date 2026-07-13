---
UID: NF:sensorsapi.ISensorEvents.OnEvent
title: ISensorEvents::OnEvent (sensorsapi.h)
description: Provides custom event notifications.
helpviewer_keywords: ["ISensorEvents interface","OnEvent method","ISensorEvents.OnEvent","ISensorEvents::OnEvent","OnEvent","OnEvent method","OnEvent method","ISensorEvents interface","sensorsapi/ISensorEvents::OnEvent","winsensors_com_ref.isensorevents_onevent"]
old-location: winsensors_com_ref\isensorevents_onevent.htm
tech.root: winsensors
ms.assetid: 7dfe25d1-dc0e-4e97-8dad-ca66a829aa4c
ms.date: 09/19/2025
ms.keywords: ISensorEvents interface,OnEvent method, ISensorEvents.OnEvent, ISensorEvents::OnEvent, OnEvent, OnEvent method, OnEvent method,ISensorEvents interface, sensorsapi/ISensorEvents::OnEvent, winsensors_com_ref.isensorevents_onevent
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
 - ISensorEvents::OnEvent
 - sensorsapi/ISensorEvents::OnEvent
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
 - ISensorEvents.OnEvent
---

# ISensorEvents::OnEvent


## -description

> [!IMPORTANT]
> Use the [UWP Sensor API](/windows/uwp/devices-sensors/sensors) instead.
>
> The COM-based Sensor API is deprecated and should not be used in new applications. No additional features or enhancements are planned, and support will be limited.

Provides custom event notifications.

## -parameters

### -param pSensor [in]

Pointer to the <a href="/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor">ISensor</a> interface that represents the sensor that raised the event.

### -param eventID [in]

<b>REFGUID</b> that identifies the event.

### -param pEventData [in]

Pointer to the <a href="/previous-versions//ms740012(v=vs.85)">IPortableDeviceValues</a> interface that contains the event data.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This callback method receives custom event notifications. Custom events are defined by sensor providers. Platform-defined event IDs are defined in Sensors.h.

To receive new data from a sensor, use the <a href="/windows/desktop/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated">OnDataUpdated Method</a>.


#### Examples

For an example of how to receive sensor events, see <a href="/windows/desktop/SensorsAPI/using-sensor-api-events">Using Sensor API Events</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents">ISensorEvents</a>