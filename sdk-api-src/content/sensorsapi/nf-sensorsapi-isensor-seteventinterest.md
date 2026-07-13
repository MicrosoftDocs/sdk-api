---
UID: NF:sensorsapi.ISensor.SetEventInterest
title: ISensor::SetEventInterest (sensorsapi.h)
description: Specifies the list of sensor events to receive.
helpviewer_keywords: ["ISensor interface","SetEventInterest method","ISensor.SetEventInterest","ISensor::SetEventInterest","SetEventInterest","SetEventInterest method","SetEventInterest method","ISensor interface","sensorsapi/ISensor::SetEventInterest","winsensors_com_ref.isensor_seteventinterest"]
old-location: winsensors_com_ref\isensor_seteventinterest.htm
tech.root: winsensors
ms.assetid: d3c2d8b9-6511-41ff-9734-92f47825bbcd
ms.date: 09/19/2025
ms.keywords: ISensor interface,SetEventInterest method, ISensor.SetEventInterest, ISensor::SetEventInterest, SetEventInterest, SetEventInterest method, SetEventInterest method,ISensor interface, sensorsapi/ISensor::SetEventInterest, winsensors_com_ref.isensor_seteventinterest
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
 - ISensor::SetEventInterest
 - sensorsapi/ISensor::SetEventInterest
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
 - ISensor.SetEventInterest
---

# ISensor::SetEventInterest


## -description

> [!IMPORTANT]
> Use the [UWP Sensor API](/windows/uwp/devices-sensors/sensors) instead.
>
> The COM-based Sensor API is deprecated and should not be used in new applications. No additional features or enhancements are planned, and support will be limited.

Specifies the list of sensor events to receive.

## -parameters

### -param pValues [in]

Pointer to an array of <b>GUID</b>s. Each <b>GUID</b> represents an event to receive. Set to <b>NULL</b> to receive all data-updated events and all custom events.

### -param count [in]

The count of <b>GUID</b>s in the array pointed to by <i>pValues</i>. Set to zero when <i>pValues</i> is <b>NULL</b>.

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

Each sensor event is represented by a <b>GUID</b>. This method takes, as an array of <b>GUID</b>s, the list of events that you want to receive.


#### Examples

For an example of how to set event interest, see <a href="/windows/desktop/SensorsAPI/using-sensor-api-events">Using Sensor API Events</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/sensorsapi/nf-sensorsapi-isensor-geteventinterest">GetEventInterest</a>



<a href="/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor">ISensor</a>