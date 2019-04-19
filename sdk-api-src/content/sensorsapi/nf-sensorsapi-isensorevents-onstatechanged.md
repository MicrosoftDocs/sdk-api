---
UID: NF:sensorsapi.ISensorEvents.OnStateChanged
title: ISensorEvents::OnStateChanged (sensorsapi.h)
author: windows-sdk-content
description: Provides a notification that a sensor state has changed.
old-location: winsensors_com_ref\isensorevents_onstatechanged.htm
tech.root: SensorsAPI
ms.assetid: fb995dba-23aa-4a09-b411-7e95019535ce
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISensorEvents interface,OnStateChanged method, ISensorEvents.OnStateChanged, ISensorEvents::OnStateChanged, OnStateChanged, OnStateChanged method, OnStateChanged method,ISensorEvents interface, sensorsapi/ISensorEvents::OnStateChanged, winsensors_com_ref.isensorevents_onstatechanged
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
 - ISensorEvents.OnStateChanged
product: Windows
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

Pointer to the <a href="https://msdn.microsoft.com/3216afbb-d524-486d-99ad-0ee0cfb884e0">ISensor</a> interface of the sensor that raised the event.


### -param state [in]


<a href="https://msdn.microsoft.com/en-us/library/Dd318905(v=VS.85).aspx">SensorState</a> containing the new state.


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




<a href="https://msdn.microsoft.com/41acbb4f-b4f8-4573-a993-ed93ec9494f0">ISensorEvents</a>
 

 

