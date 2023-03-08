---
UID: NF:cscobj.IOfflineFilesEvents.Ping
title: IOfflineFilesEvents::Ping (cscobj.h)
description: This event is delivered to all registered event subscribers on a periodic basis.
helpviewer_keywords: ["IOfflineFilesEvents interface [Offline Files]","Ping method","IOfflineFilesEvents.Ping","IOfflineFilesEvents::Ping","Ping","Ping method [Offline Files]","Ping method [Offline Files]","IOfflineFilesEvents interface","cscobj/IOfflineFilesEvents::Ping","of.iofflinefilesevents_ping"]
old-location: of\iofflinefilesevents_ping.htm
tech.root: of
ms.assetid: edde2f37-f082-4382-8908-181bc42d30ef
ms.date: 12/05/2018
ms.keywords: IOfflineFilesEvents interface [Offline Files],Ping method, IOfflineFilesEvents.Ping, IOfflineFilesEvents::Ping, Ping, Ping method [Offline Files], Ping method [Offline Files],IOfflineFilesEvents interface, cscobj/IOfflineFilesEvents::Ping, of.iofflinefilesevents_ping
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
 - IOfflineFilesEvents::Ping
 - cscobj/IOfflineFilesEvents::Ping
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
 - IOfflineFilesEvents.Ping
---

# IOfflineFilesEvents::Ping


## -description

This event is delivered to all registered event subscribers on a periodic basis.



## -returns

The return value is ignored.

## -remarks

If a recipient does not respond, a COM error is received by the Offline Files service, and the subscriber's connection is deleted.  This is how the Offline Files service detects event subscriber processes that have terminated before calling <a href="/windows/desktop/api/ocidl/nf-ocidl-iconnectionpoint-unadvise">IConnectionPoint::Unadvise</a>.

This event cannot be filtered out by using the <a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefileseventsfilter">IOfflineFilesEventsFilter</a> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesevents">IOfflineFilesEvents</a>
