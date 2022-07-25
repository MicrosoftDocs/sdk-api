---
UID: NF:cscobj.IOfflineFilesEvents.DataLost
title: IOfflineFilesEvents::DataLost (cscobj.h)
description: Reports that one or more events destined for this event sink have been lost and will not be delivered.
helpviewer_keywords: ["DataLost","DataLost method [Offline Files]","DataLost method [Offline Files]","IOfflineFilesEvents interface","IOfflineFilesEvents interface [Offline Files]","DataLost method","IOfflineFilesEvents.DataLost","IOfflineFilesEvents::DataLost","cscobj/IOfflineFilesEvents::DataLost","of.iofflinefilesevents_datalost"]
old-location: of\iofflinefilesevents_datalost.htm
tech.root: of
ms.assetid: da0414dd-2acb-48d9-ac84-66bb1f7ccbef
ms.date: 12/05/2018
ms.keywords: DataLost, DataLost method [Offline Files], DataLost method [Offline Files],IOfflineFilesEvents interface, IOfflineFilesEvents interface [Offline Files],DataLost method, IOfflineFilesEvents.DataLost, IOfflineFilesEvents::DataLost, cscobj/IOfflineFilesEvents::DataLost, of.iofflinefilesevents_datalost
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
 - IOfflineFilesEvents::DataLost
 - cscobj/IOfflineFilesEvents::DataLost
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
 - IOfflineFilesEvents.DataLost
---

# IOfflineFilesEvents::DataLost


## -description

Reports that one or more events destined for this event sink have been lost and will not be delivered. The receipt of this event indicates that the service is attempting to deliver events to this event sink faster than the sink is consuming them.



## -returns

The return value is ignored.

## -remarks

This event cannot be filtered out by using the <a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefileseventsfilter">IOfflineFilesEventsFilter</a> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesevents">IOfflineFilesEvents</a>
