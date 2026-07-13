---
UID: NF:tuner.ITuner.TriggerSignalEvents
title: ITuner::TriggerSignalEvents (tuner.h)
description: The TriggerSignalEvents method enables the tuner to raise an event when the status of the signal changes.
helpviewer_keywords: ["ITuner interface [Microsoft TV Technologies]","TriggerSignalEvents method","ITuner.TriggerSignalEvents","ITuner::TriggerSignalEvents","ITunerTriggerSignalEvents","TriggerSignalEvents","TriggerSignalEvents method [Microsoft TV Technologies]","TriggerSignalEvents method [Microsoft TV Technologies]","ITuner interface","mstv.ituner_triggersignalevents","tuner/ITuner::TriggerSignalEvents"]
old-location: mstv\ituner_triggersignalevents.htm
tech.root: mstv
ms.assetid: 9cff8ee2-d474-4ea5-a284-608eb0288c9f
ms.date: 12/05/2018
ms.keywords: ITuner interface [Microsoft TV Technologies],TriggerSignalEvents method, ITuner.TriggerSignalEvents, ITuner::TriggerSignalEvents, ITunerTriggerSignalEvents, TriggerSignalEvents, TriggerSignalEvents method [Microsoft TV Technologies], TriggerSignalEvents method [Microsoft TV Technologies],ITuner interface, mstv.ituner_triggersignalevents, tuner/ITuner::TriggerSignalEvents
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITuner::TriggerSignalEvents
 - tuner/ITuner::TriggerSignalEvents
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - ITuner.TriggerSignalEvents
---

# ITuner::TriggerSignalEvents


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>TriggerSignalEvents</b> method enables the tuner to raise an event when the status of the signal changes.

## -parameters

### -param Interval [in]

Specifies the time-out interval in milliseconds.

## -returns

When the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -remarks

If the signal status does not change by the time that the time-out interval expires, the tuner raises the signal-status-change event at the end of the time-out interval. If the caller specifies the interval to be INFINITE, the tuner does not raise the event until the signal status changes, regardless of how much time elapses before the change occurs. Specifying a value of 0 raises the signal-status-change event immediately, regardless of whether the signal status has changed.

Each call to <b>TriggerSignalEvents</b> enables the event to be raised only one time. To raise the event multiple times in response to a series of signal-status changes requires a succession of calls to <b>TriggerSignalEvents</b>.

Multiple event sink objects can wait for the tuner to raise an event that occurs when the signal status changes. For more information, see <a href="/previous-versions/dd376294(v=vs.85)">IBroadcastEvent Interface</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituner">ITuner Interface</a>