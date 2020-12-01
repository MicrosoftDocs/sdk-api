---
UID: NN:pla.ISchedule
title: ISchedule (pla.h)
description: Specifies when the data collector set runs.To get this interface, call the IScheduleCollection::CreateSchedule method.
helpviewer_keywords: ["ISchedule","ISchedule interface [PLA]","ISchedule interface [PLA]","described","base.ischedule","pla.ischedule","pla/ISchedule"]
old-location: pla\ischedule.htm
tech.root: PLA
ms.assetid: b02043c6-5010-45a1-a4a4-ce30cbf0dba0
ms.date: 12/05/2018
ms.keywords: ISchedule, ISchedule interface [PLA], ISchedule interface [PLA],described, base.ischedule, pla.ischedule, pla/ISchedule
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
 - ISchedule
 - pla/ISchedule
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
 - ISchedule
---

# ISchedule interface


## -description

Specifies when the data collector set runs.

To get this interface, call the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ischedulecollection-createschedule">IScheduleCollection::CreateSchedule</a> method.

## -remarks

To create the object from a script, use the Pla.Schedule program identifier.

PLA uses the schedule when the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_schedulesenabled">IDataCollectorSet::SchedulesEnabled</a> property is VARIANT_TRUE.

For an example that shows the XML that you can use to initialize this object if you call the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-setxml">IDataCollectorSet::SetXml</a> method, see the Remarks section of <a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollectorset">IDataCollectorSet</a>.  When you specify the XML to create the object, you can specify only the elements for the properties that you want to set. If you do not specify a property, PLA provides a default value. When you retrieve the XML for the set, the XML includes all elements.