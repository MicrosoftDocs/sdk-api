---
UID: NF:sensorsapi.ISensorManager.SetEventSink
title: ISensorManager::SetEventSink (sensorsapi.h)
description: Specifies the interface through which to receive sensor manager event notifications.
helpviewer_keywords: ["ISensorManager interface","SetEventSink method","ISensorManager.SetEventSink","ISensorManager::SetEventSink","SetEventSink","SetEventSink method","SetEventSink method","ISensorManager interface","sensorsapi/ISensorManager::SetEventSink","winsensors_com_ref.isensormanager_seteventsink"]
old-location: winsensors_com_ref\isensormanager_seteventsink.htm
tech.root: winsensors
ms.assetid: 270f0943-dc6a-47df-b1bd-ecfbfcafc4c8
ms.date: 09/19/2025
ms.keywords: ISensorManager interface,SetEventSink method, ISensorManager.SetEventSink, ISensorManager::SetEventSink, SetEventSink, SetEventSink method, SetEventSink method,ISensorManager interface, sensorsapi/ISensorManager::SetEventSink, winsensors_com_ref.isensormanager_seteventsink
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
 - ISensorManager::SetEventSink
 - sensorsapi/ISensorManager::SetEventSink
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
 - ISensorManager.SetEventSink
---

# ISensorManager::SetEventSink


## -description

> [!IMPORTANT]
> Use the [UWP Sensor API](/windows/uwp/devices-sensors/sensors) instead.
>
> The COM-based Sensor API is deprecated and should not be used in new applications. No additional features or enhancements are planned, and support will be limited.

Specifies the interface through which to receive sensor manager event notifications.

## -parameters

### -param pEvents [in]

Pointer to the <a href="/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanagerevents">ISensorManagerEvents</a> callback interface that receives the event notifications. Set to <b>NULL</b> to stop receiving event notifications.

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

<a href="/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager">ISensorManager</a>