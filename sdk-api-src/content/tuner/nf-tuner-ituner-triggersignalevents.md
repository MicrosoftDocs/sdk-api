---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ITuner::TriggerSignalEvents


## -description



The <b>TriggerSignalEvents</b> method enables the tuner to raise an event when the status of the signal changes.




## -parameters




### -param Interval [in]

Specifies the time-out interval in milliseconds.


## -returns



When the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -remarks



If the signal status does not change by the time that the time-out interval expires, the tuner raises the signal-status-change event at the end of the time-out interval. If the caller specifies the interval to be INFINITE, the tuner does not raise the event until the signal status changes, regardless of how much time elapses before the change occurs. Specifying a value of 0 raises the signal-status-change event immediately, regardless of whether the signal status has changed.

Each call to <b>TriggerSignalEvents</b> enables the event to be raised only one time. To raise the event multiple times in response to a series of signal-status changes requires a succession of calls to <b>TriggerSignalEvents</b>.

Multiple event sink objects can wait for the tuner to raise an event that occurs when the signal status changes. For more information, see <a href="https://msdn.microsoft.com/90d4fbc7-d552-460b-96b2-77e2347af716">IBroadcastEvent Interface</a>.




## -see-also




<a href="https://msdn.microsoft.com/1bc965a5-6bc9-488a-a2f9-f35d0cfbcccd">ITuner Interface</a>
 

 

