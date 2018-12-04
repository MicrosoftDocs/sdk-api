---
UID: NF:sensorsapi.ISensor.SetEventSink
title: ISensor::SetEventSink
author: windows-sdk-content
description: Specifies the interface through which to receive sensor event notifications.
old-location: winsensors_com_ref\isensor_seteventsink.htm
tech.root: SensorsAPI
ms.assetid: 8e2f7edc-894f-4258-8948-2a3d4df532c3
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: ISensor interface,SetEventSink method, ISensor.SetEventSink, ISensor::SetEventSink, SetEventSink, SetEventSink method, SetEventSink method,ISensor interface, sensorsapi/ISensor::SetEventSink, winsensors_com_ref.isensor_seteventsink
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ISensor.SetEventSink
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISensor::SetEventSink


## -description


Specifies the interface through which to receive sensor event notifications.


## -parameters




### -param pEvents [in]

Pointer to the <a href="https://msdn.microsoft.com/41acbb4f-b4f8-4573-a993-ed93ec9494f0">ISensorEvents</a> callback interface that receives the event notifications. Set to <b>NULL</b> to cancel event notifications.


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



Specify the events to receive by calling <a href="https://msdn.microsoft.com/d3c2d8b9-6511-41ff-9734-92f47825bbcd">SetEventInterest</a>. You can retrieve the current event interest list by calling <a href="https://msdn.microsoft.com/8324817e-c310-4b90-b5b4-c7e113e3502e">GetEventInterest</a>.


#### Examples

For an example of how to set the event sink, see <a href="https://msdn.microsoft.com/0c396d54-cb2e-4b07-999f-3f4001db2a02">Using Sensor API Events</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/3216afbb-d524-486d-99ad-0ee0cfb884e0">ISensor</a>
 

 

