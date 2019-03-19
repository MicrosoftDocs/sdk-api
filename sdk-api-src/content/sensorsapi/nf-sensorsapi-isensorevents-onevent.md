---
UID: NF:sensorsapi.ISensorEvents.OnEvent
title: ISensorEvents::OnEvent (sensorsapi.h)
author: windows-sdk-content
description: Provides custom event notifications.
old-location: winsensors_com_ref\isensorevents_onevent.htm
tech.root: SensorsAPI
ms.assetid: 7dfe25d1-dc0e-4e97-8dad-ca66a829aa4c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ISensorEvents interface,OnEvent method, ISensorEvents.OnEvent, ISensorEvents::OnEvent, OnEvent, OnEvent method, OnEvent method,ISensorEvents interface, sensorsapi/ISensorEvents::OnEvent, winsensors_com_ref.isensorevents_onevent
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
 - ISensorEvents.OnEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISensorEvents::OnEvent


## -description


Provides custom event notifications.


## -parameters




### -param pSensor [in]

Pointer to the <a href="https://msdn.microsoft.com/3216afbb-d524-486d-99ad-0ee0cfb884e0">ISensor</a> interface that represents the sensor that raised the event.


### -param eventID [in]

<b>REFGUID</b> that identifies the event.


### -param pEventData [in]

Pointer to the <a href="http://go.microsoft.com/fwlink/p/?linkid=134660">IPortableDeviceValues</a> interface that contains the event data.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This callback method receives custom event notifications. Custom events are defined by sensor providers. Platform-defined event IDs are defined in Sensors.h.

To receive new data from a sensor, use the <a href="https://msdn.microsoft.com/dda03a66-ffdb-4f1f-a6e4-17075eab7e00">OnDataUpdated Method</a>.


#### Examples

For an example of how to receive sensor events, see <a href="https://msdn.microsoft.com/0c396d54-cb2e-4b07-999f-3f4001db2a02">Using Sensor API Events</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/41acbb4f-b4f8-4573-a993-ed93ec9494f0">ISensorEvents</a>
 

 

