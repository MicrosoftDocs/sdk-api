---
UID: NF:sensorsapi.ISensorEvents.OnStateChanged
title: ISensorEvents::OnStateChanged (sensorsapi.h)
description: Provides a notification that a sensor state has changed.helpviewer_keywords: ["ISensorEvents interface","OnStateChanged method","ISensorEvents.OnStateChanged","ISensorEvents::OnStateChanged","OnStateChanged","OnStateChanged method","OnStateChanged method","ISensorEvents interface","sensorsapi/ISensorEvents::OnStateChanged","winsensors_com_ref.isensorevents_onstatechanged"]
old-location: winsensors_com_ref\isensorevents_onstatechanged.htm
tech.root: SensorsAPI
ms.assetid: fb995dba-23aa-4a09-b411-7e95019535ce
ms.date: 12/05/2018
ms.keywords: ISensorEvents interface,OnStateChanged method, ISensorEvents.OnStateChanged, ISensorEvents::OnStateChanged, OnStateChanged, OnStateChanged method, OnStateChanged method,ISensorEvents interface, sensorsapi/ISensorEvents::OnStateChanged, winsensors_com_ref.isensorevents_onstatechanged
f1_keywords:
- sensorsapi/ISensorEvents.OnStateChanged
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- sensorsapi.dll
api_name:
- ISensorEvents.OnStateChanged
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISensorEvents::OnStateChanged


## -description


Provides a notification that a sensor state has changed.


## -parameters




### -param pSensor [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor">ISensor</a> interface of the sensor that raised the event.


### -param state [in]


<a href="https://docs.microsoft.com/windows/win32/api/sensorsapi/ne-sensorsapi-sensorstate">SensorState</a> containing the new state.


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




<a href="https://docs.microsoft.com/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents">ISensorEvents</a>
 

 

