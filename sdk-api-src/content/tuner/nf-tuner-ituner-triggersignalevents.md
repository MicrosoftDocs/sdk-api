---
UID: NF:tuner.ITuner.TriggerSignalEvents
title: ITuner::TriggerSignalEvents
author: windows-sdk-content
description: The TriggerSignalEvents method enables the tuner to raise an event when the status of the signal changes.
old-location: mstv\ituner_triggersignalevents.htm
old-project: mstv
ms.assetid: 9cff8ee2-d474-4ea5-a284-608eb0288c9f
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ITuner interface [Microsoft TV Technologies],TriggerSignalEvents method, ITuner.TriggerSignalEvents, ITuner::TriggerSignalEvents, ITunerTriggerSignalEvents, TriggerSignalEvents, TriggerSignalEvents method [Microsoft TV Technologies], TriggerSignalEvents method [Microsoft TV Technologies],ITuner interface, mstv.ituner_triggersignalevents, tuner/ITuner::TriggerSignalEvents
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - ITuner.TriggerSignalEvents
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
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
 

 

