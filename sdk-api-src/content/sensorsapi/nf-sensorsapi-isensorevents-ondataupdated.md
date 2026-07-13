---
UID: NF:sensorsapi.ISensorEvents.OnDataUpdated
title: ISensorEvents::OnDataUpdated (sensorsapi.h)
description: Provides sensor event data.
helpviewer_keywords: ["ISensorEvents interface","OnDataUpdated method","ISensorEvents.OnDataUpdated","ISensorEvents::OnDataUpdated","OnDataUpdated","OnDataUpdated method","OnDataUpdated method","ISensorEvents interface","sensorsapi/ISensorEvents::OnDataUpdated","winsensors_com_ref.isensorevents_ondataupdated"]
old-location: winsensors_com_ref\isensorevents_ondataupdated.htm
tech.root: winsensors
ms.assetid: dda03a66-ffdb-4f1f-a6e4-17075eab7e00
ms.date: 09/19/2025
ms.keywords: ISensorEvents interface,OnDataUpdated method, ISensorEvents.OnDataUpdated, ISensorEvents::OnDataUpdated, OnDataUpdated, OnDataUpdated method, OnDataUpdated method,ISensorEvents interface, sensorsapi/ISensorEvents::OnDataUpdated, winsensors_com_ref.isensorevents_ondataupdated
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
 - ISensorEvents::OnDataUpdated
 - sensorsapi/ISensorEvents::OnDataUpdated
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
 - ISensorEvents.OnDataUpdated
---

# ISensorEvents::OnDataUpdated


## -description

> [!IMPORTANT]
> Use the [UWP Sensor API](/windows/uwp/devices-sensors/sensors) instead.
>
> The COM-based Sensor API is deprecated and should not be used in new applications. No additional features or enhancements are planned, and support will be limited.

Provides sensor event data.

## -parameters

### -param pSensor [in]

Pointer to the <a href="/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor">ISensor</a> interface of the sensor that raised the event.

### -param pNewData [in]

Pointer to the <a href="/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport">ISensorDataReport</a> interface that contains the event data.

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

## -see-also

<a href="/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents">ISensorEvents</a>