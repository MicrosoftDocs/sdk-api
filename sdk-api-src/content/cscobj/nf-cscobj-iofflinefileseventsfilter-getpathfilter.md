---
UID: NF:cscobj.IOfflineFilesEventsFilter.GetPathFilter
title: IOfflineFilesEventsFilter::GetPathFilter (cscobj.h)
description: Retrieves a UNC path string and a scope indicator describing which path-based events should be delivered to this event sink.
helpviewer_keywords: ["GetPathFilter","GetPathFilter method [Offline Files]","GetPathFilter method [Offline Files]","IOfflineFilesEventsFilter interface","IOfflineFilesEventsFilter interface [Offline Files]","GetPathFilter method","IOfflineFilesEventsFilter.GetPathFilter","IOfflineFilesEventsFilter::GetPathFilter","cscobj/IOfflineFilesEventsFilter::GetPathFilter","of.iofflinefileseventsfilter_getpathfilter"]
old-location: of\iofflinefileseventsfilter_getpathfilter.htm
tech.root: of
ms.assetid: 0b9d8339-3daa-4f0c-8a52-59e06b663163
ms.date: 12/05/2018
ms.keywords: GetPathFilter, GetPathFilter method [Offline Files], GetPathFilter method [Offline Files],IOfflineFilesEventsFilter interface, IOfflineFilesEventsFilter interface [Offline Files],GetPathFilter method, IOfflineFilesEventsFilter.GetPathFilter, IOfflineFilesEventsFilter::GetPathFilter, cscobj/IOfflineFilesEventsFilter::GetPathFilter, of.iofflinefileseventsfilter_getpathfilter
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
 - IOfflineFilesEventsFilter::GetPathFilter
 - cscobj/IOfflineFilesEventsFilter::GetPathFilter
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
 - IOfflineFilesEventsFilter.GetPathFilter
---

# IOfflineFilesEventsFilter::GetPathFilter


## -description

Retrieves a UNC path string and a scope indicator describing which path-based events should be delivered to this event sink.

## -parameters

### -param ppszFilter [out]

Receives a fully qualified UNC path string identifying the path associated with the filter. The memory for this string must be allocated using the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a> function.

### -param pMatch [out]

Receives an <a href="/windows/desktop/api/cscobj/ne-cscobj-offlinefiles_pathfilter_match">OFFLINEFILES_PATHFILTER_MATCH</a> enumeration  value indicating which descendants of the filter path are to be included in the set of events delivered to the event sink.

## -returns

Return <b>S_OK</b> if implemented, <b>E_NOTIMPL</b> if not implemented.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefileseventsfilter">IOfflineFilesEventsFilter</a>