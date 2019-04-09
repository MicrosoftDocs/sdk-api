---
UID: NF:sensorsapi.ISensorManagerEvents.OnSensorEnter
title: ISensorManagerEvents::OnSensorEnter (sensorsapi.h)
author: windows-sdk-content
description: Provides notification when a sensor device is connected.
old-location: winsensors_com_ref\isensormanagerevents_onsensorenter.htm
tech.root: SensorsAPI
ms.assetid: 1316e3b0-9677-4575-a3b8-53fa57295987
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISensorManagerEvents interface,OnSensorEnter method, ISensorManagerEvents.OnSensorEnter, ISensorManagerEvents::OnSensorEnter, OnSensorEnter, OnSensorEnter method, OnSensorEnter method,ISensorManagerEvents interface, sensorsapi/ISensorManagerEvents::OnSensorEnter, winsensors_com_ref.isensormanagerevents_onsensorenter, winsensors_com_ref.isensormanagerevents_sensorenter
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISensorManagerEvents::OnSensorEnter


## -description


Provides notification when a sensor device is connected.


## -parameters




### -param pSensor [in]

A pointer to the <a href="https://msdn.microsoft.com/3216afbb-d524-486d-99ad-0ee0cfb884e0">ISensor</a> interface of the sensor that was connected.


### -param state [in]


<a href="https://msdn.microsoft.com/en-us/library/Dd318905(v=VS.85).aspx">SensorState</a> indicating the current state of the sensor.


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



To know when a sensor is disconnected, subscribe to the <a href="https://msdn.microsoft.com/541ef7a4-c238-4fc5-9b2d-1fadb1472b2d">ISensorEvents::OnLeave</a> event.




## -see-also




<a href="https://msdn.microsoft.com/b111a717-00c0-47cb-be6a-3050d54cd2ec">ISensorManagerEvents</a>
 

 

