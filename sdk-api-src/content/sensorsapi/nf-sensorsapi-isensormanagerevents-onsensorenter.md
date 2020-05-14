---
UID: NF:sensorsapi.ISensorManagerEvents.OnSensorEnter
title: ISensorManagerEvents::OnSensorEnter (sensorsapi.h)
description: Provides notification when a sensor device is connected.
helpviewer_keywords: ["ISensorManagerEvents interface","OnSensorEnter method","ISensorManagerEvents.OnSensorEnter","ISensorManagerEvents::OnSensorEnter","OnSensorEnter","OnSensorEnter method","OnSensorEnter method","ISensorManagerEvents interface","sensorsapi/ISensorManagerEvents::OnSensorEnter","winsensors_com_ref.isensormanagerevents_onsensorenter","winsensors_com_ref.isensormanagerevents_sensorenter"]
old-location: winsensors_com_ref\isensormanagerevents_onsensorenter.htm
tech.root: SensorsAPI
ms.assetid: 1316e3b0-9677-4575-a3b8-53fa57295987
ms.date: 12/05/2018
ms.keywords: ISensorManagerEvents interface,OnSensorEnter method, ISensorManagerEvents.OnSensorEnter, ISensorManagerEvents::OnSensorEnter, OnSensorEnter, OnSensorEnter method, OnSensorEnter method,ISensorManagerEvents interface, sensorsapi/ISensorManagerEvents::OnSensorEnter, winsensors_com_ref.isensormanagerevents_onsensorenter, winsensors_com_ref.isensormanagerevents_sensorenter
f1_keywords:
- sensorsapi/ISensorManagerEvents.OnSensorEnter
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
- ISensorManagerEvents.OnSensorEnter
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISensorManagerEvents::OnSensorEnter


## -description


Provides notification when a sensor device is connected.


## -parameters




### -param pSensor [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor">ISensor</a> interface of the sensor that was connected.


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



To know when a sensor is disconnected, subscribe to the <a href="https://docs.microsoft.com/windows/desktop/api/sensorsapi/nf-sensorsapi-isensorevents-onleave">ISensorEvents::OnLeave</a> event.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanagerevents">ISensorManagerEvents</a>
 

 

