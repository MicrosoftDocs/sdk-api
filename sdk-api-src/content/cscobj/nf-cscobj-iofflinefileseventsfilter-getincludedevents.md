---
UID: NF:cscobj.IOfflineFilesEventsFilter.GetIncludedEvents
title: IOfflineFilesEventsFilter::GetIncludedEvents (cscobj.h)
description: Retrieves an array of OFFLINEFILES_EVENTS enumeration values describing which events should be received by the event sink.
helpviewer_keywords: ["GetIncludedEvents","GetIncludedEvents method [Offline Files]","GetIncludedEvents method [Offline Files]","IOfflineFilesEventsFilter interface","IOfflineFilesEventsFilter interface [Offline Files]","GetIncludedEvents method","IOfflineFilesEventsFilter.GetIncludedEvents","IOfflineFilesEventsFilter::GetIncludedEvents","cscobj/IOfflineFilesEventsFilter::GetIncludedEvents","of.iofflinefileseventsfilter_getincludedevents"]
old-location: of\iofflinefileseventsfilter_getincludedevents.htm
tech.root: of
ms.assetid: ecb10da3-7566-43f7-8349-f94e59e12907
ms.date: 12/05/2018
ms.keywords: GetIncludedEvents, GetIncludedEvents method [Offline Files], GetIncludedEvents method [Offline Files],IOfflineFilesEventsFilter interface, IOfflineFilesEventsFilter interface [Offline Files],GetIncludedEvents method, IOfflineFilesEventsFilter.GetIncludedEvents, IOfflineFilesEventsFilter::GetIncludedEvents, cscobj/IOfflineFilesEventsFilter::GetIncludedEvents, of.iofflinefileseventsfilter_getincludedevents
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOfflineFilesEventsFilter::GetIncludedEvents
 - cscobj/IOfflineFilesEventsFilter::GetIncludedEvents
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesEventsFilter.GetIncludedEvents
---

# IOfflineFilesEventsFilter::GetIncludedEvents


## -description

Retrieves an array of <a href="/windows/desktop/api/cscobj/ne-cscobj-offlinefiles_events">OFFLINEFILES_EVENTS</a> enumeration values describing which events should be received by the event sink. If a particular event is specified both in <b>IOfflineFilesEventsFilter::GetIncludedEvents</b> and <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefileseventsfilter-getexcludedevents">IOfflineFilesEventsFilter::GetExcludedEvents</a>, the event is excluded from this event sink.

## -parameters

### -param cElements [in]

Specifies the maximum number of elements that can be stored in the array referenced by the <i>prgEvents</i> parameter.

### -param prgEvents [out]

Contains the address of an array of <a href="/windows/desktop/api/cscobj/ne-cscobj-offlinefiles_events">OFFLINEFILES_EVENTS</a> enumeration values.  Place the <b>OFFLINEFILES_EVENT_XXXXXX</b> identifier in an array entry to specify that the corresponding event is desired by this event sink.

### -param pcEvents [out]

Receives the actual number of elements written to the array referenced by the <i>prgEvents</i> parameter.

## -returns

Return <b>S_OK</b> if implemented, <b>E_NOTIMPL</b> if not implemented.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefileseventsfilter">IOfflineFilesEventsFilter</a>



<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefileseventsfilter-getexcludedevents">IOfflineFilesEventsFilter::GetExcludedEvents</a>



<a href="/windows/desktop/api/cscobj/ne-cscobj-offlinefiles_events">OFFLINEFILES_EVENTS</a>