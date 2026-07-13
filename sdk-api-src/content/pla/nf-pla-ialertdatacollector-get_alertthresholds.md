---
UID: NF:pla.IAlertDataCollector.get_AlertThresholds
title: IAlertDataCollector::get_AlertThresholds (pla.h)
description: Retrieves or sets a list of performance counters and thresholds to monitor. (Get)
helpviewer_keywords: ["AlertThresholds property [PLA]","AlertThresholds property [PLA]","IAlertDataCollector interface","IAlertDataCollector interface [PLA]","AlertThresholds property","IAlertDataCollector.AlertThresholds","IAlertDataCollector.get_AlertThresholds","IAlertDataCollector::AlertThresholds","IAlertDataCollector::get_AlertThresholds","IAlertDataCollector::put_AlertThresholds","base.ialertdatacollector_alertthresholds","get_AlertThresholds","pla.ialertdatacollector_alertthresholds","pla/IAlertDataCollector::AlertThresholds","pla/IAlertDataCollector::get_AlertThresholds","pla/IAlertDataCollector::put_AlertThresholds"]
old-location: pla\ialertdatacollector_alertthresholds.htm
tech.root: PLA
ms.assetid: e0d504ea-58d4-48fd-9baf-851505d6d3ac
ms.date: 12/05/2018
ms.keywords: AlertThresholds property [PLA], AlertThresholds property [PLA],IAlertDataCollector interface, IAlertDataCollector interface [PLA],AlertThresholds property, IAlertDataCollector.AlertThresholds, IAlertDataCollector.get_AlertThresholds, IAlertDataCollector::AlertThresholds, IAlertDataCollector::get_AlertThresholds, IAlertDataCollector::put_AlertThresholds, base.ialertdatacollector_alertthresholds, get_AlertThresholds, pla.ialertdatacollector_alertthresholds, pla/IAlertDataCollector::AlertThresholds, pla/IAlertDataCollector::get_AlertThresholds, pla/IAlertDataCollector::put_AlertThresholds
req.header: pla.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Pla.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAlertDataCollector::get_AlertThresholds
 - pla/IAlertDataCollector::get_AlertThresholds
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - IAlertDataCollector.AlertThresholds
 - IAlertDataCollector.get_AlertThresholds
 - IAlertDataCollector.put_AlertThresholds
---

## -description

Retrieves or sets a list of performance counters and thresholds to monitor as a SAFEARRAY of BSTR. For example, `L"\Memory\Committed Bytes>549755813888"`.

This property is read/write.

## -parameters

## -remarks

You must specify at least one alert threshold. If the counter value crosses the specified threshold value, PLA performs one or more of the following actions:

<ul>
<li>Logs event 2031 to the  Microsoft-Windows-Diagnosis-PLA/Operational event log if the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ialertdatacollector-get_eventlog">IAlertDataCollector::EventLog</a>  property is true.</li>
<li>Starts the task in the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ialertdatacollector-get_task">IAlertDataCollector::Task</a>  property, if specified.</li>
<li>Triggers the data collector set specified in the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ialertdatacollector-get_triggerdatacollectorset">IAlertDataCollector::TriggerDataCollectorSet</a>  property to run, if specified.</li>
</ul>
If you use XML to define the alert, you must use "&amp;gt;" for the greater than sign (&gt;) and "&amp;lt;" for the less than sign (&lt;).

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-ialertdatacollector">IAlertDataCollector</a>
