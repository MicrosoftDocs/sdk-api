---
UID: NF:bdatif.IGuideDataEvent.ScheduleEntryChanged
title: IGuideDataEvent::ScheduleEntryChanged (bdatif.h)
description: The ScheduleEntryChanged method is called by the TIF when information about one or more schedule entries has changed.
helpviewer_keywords: ["IGuideDataEvent interface [Microsoft TV Technologies]","ScheduleEntryChanged method","IGuideDataEvent.ScheduleEntryChanged","IGuideDataEvent::ScheduleEntryChanged","IGuideDataEventScheduleEntryChanged","ScheduleEntryChanged","ScheduleEntryChanged method [Microsoft TV Technologies]","ScheduleEntryChanged method [Microsoft TV Technologies]","IGuideDataEvent interface","bdatif/IGuideDataEvent::ScheduleEntryChanged","mstv.iguidedataevent_scheduleentrychanged"]
old-location: mstv\iguidedataevent_scheduleentrychanged.htm
tech.root: mstv
ms.assetid: 04c278a0-8a92-4801-9463-696beb22819e
ms.date: 12/05/2018
ms.keywords: IGuideDataEvent interface [Microsoft TV Technologies],ScheduleEntryChanged method, IGuideDataEvent.ScheduleEntryChanged, IGuideDataEvent::ScheduleEntryChanged, IGuideDataEventScheduleEntryChanged, ScheduleEntryChanged, ScheduleEntryChanged method [Microsoft TV Technologies], ScheduleEntryChanged method [Microsoft TV Technologies],IGuideDataEvent interface, bdatif/IGuideDataEvent::ScheduleEntryChanged, mstv.iguidedataevent_scheduleentrychanged
req.header: bdatif.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGuideDataEvent::ScheduleEntryChanged
 - bdatif/IGuideDataEvent::ScheduleEntryChanged
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdatif.h
api_name:
 - IGuideDataEvent.ScheduleEntryChanged
---

# IGuideDataEvent::ScheduleEntryChanged


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>ScheduleEntryChanged</b> method is called by the TIF when information about one or more schedule entries has changed.

## -parameters

### -param varScheduleEntryDescriptionID [in]

Specifies the unique identifier of the program that has changed. Call <a href="/previous-versions/windows/desktop/api/bdatif/nf-bdatif-iguidedata-getscheduleentryproperties">IGuideData::GetScheduleEntryProperties</a> to get information about the program. The value of this parameter may be an empty <b>VARIANT</b> type (VT_EMPTY); if so, examine all of the programs to determine which ones have changed.

## -returns

Return S_OK if successful, or an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/windows/desktop/api/bdatif/nn-bdatif-iguidedataevent">IGuideDataEvent Interface</a>