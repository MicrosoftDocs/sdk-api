---
UID: NF:pla.IDataCollectorSet.get_Schedules
title: IDataCollectorSet::get_Schedules (pla.h)
description: Retrieves the list of schedules that determine when the data collector set runs.
helpviewer_keywords: ["IDataCollectorSet interface [PLA]","Schedules property","IDataCollectorSet.Schedules","IDataCollectorSet.get_Schedules","IDataCollectorSet::Schedules","IDataCollectorSet::get_Schedules","Schedules property [PLA]","Schedules property [PLA]","IDataCollectorSet interface","base.idatacollectorset_get_schedules","get_Schedules","pla.idatacollectorset_get_schedules","pla/IDataCollectorSet::Schedules","pla/IDataCollectorSet::get_Schedules"]
old-location: pla\idatacollectorset_get_schedules.htm
tech.root: PLA
ms.assetid: 6654c101-5179-41db-8fd9-ae281691073f
ms.date: 12/05/2018
ms.keywords: IDataCollectorSet interface [PLA],Schedules property, IDataCollectorSet.Schedules, IDataCollectorSet.get_Schedules, IDataCollectorSet::Schedules, IDataCollectorSet::get_Schedules, Schedules property [PLA], Schedules property [PLA],IDataCollectorSet interface, base.idatacollectorset_get_schedules, get_Schedules, pla.idatacollectorset_get_schedules, pla/IDataCollectorSet::Schedules, pla/IDataCollectorSet::get_Schedules
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
 - IDataCollectorSet::get_Schedules
 - pla/IDataCollectorSet::get_Schedules
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
 - IDataCollectorSet.Schedules
 - IDataCollectorSet.get_Schedules
---

# IDataCollectorSet::get_Schedules


## -description

Retrieves the list of schedules that determine when the data collector set runs.

This property is read-only.

## -parameters

## -remarks

There can be only one instance of a data collector set running at a time; if one is already running and a second one tries to start, the second one will fail and the first one will continue.

To enable the schedules, call the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_schedulesenabled">IDataCollectorSet::SchedulesEnabled</a> property.

To manually start the data collector set, call the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-start">IDataCollectorSet::Start</a> method.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollectorset">IDataCollectorSet</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_schedulesenabled">IDataCollectorSet::SchedulesEnabled</a>