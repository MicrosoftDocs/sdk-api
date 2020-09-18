---
UID: NN:cscobj.IOfflineFilesEvents
title: IOfflineFilesEvents (cscobj.h)
description: Used to report significant events associated with Offline Files.
helpviewer_keywords: ["IOfflineFilesEvents","IOfflineFilesEvents interface [Offline Files]","IOfflineFilesEvents interface [Offline Files]","described","cscobj/IOfflineFilesEvents","of.iofflinefilesevents"]
old-location: of\iofflinefilesevents.htm
tech.root: of
ms.assetid: c0bd0033-e5e1-4d21-8d98-eb937acdd6cf
ms.date: 12/05/2018
ms.keywords: IOfflineFilesEvents, IOfflineFilesEvents interface [Offline Files], IOfflineFilesEvents interface [Offline Files],described, cscobj/IOfflineFilesEvents, of.iofflinefilesevents
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
 - IOfflineFilesEvents
 - cscobj/IOfflineFilesEvents
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
 - IOfflineFilesEvents
---

# IOfflineFilesEvents interface


## -description

 Used to report significant events associated with Offline Files.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesEvents</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOfflineFilesEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOfflineFilesEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesevents-cacheiscorrupted">CacheIsCorrupted</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesevents-cacheisfull">CacheIsFull</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesevents-cachemoved">CacheMoved</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesevents-datalost">DataLost</a>
</td>
<td align="left" width="63%">
Reports that one or more events destined for this event sink have been lost and will not be delivered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesevents-enabled">Enabled</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesevents-encryptionchanged">EncryptionChanged</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesevents-itemaddedtocache">ItemAddedToCache</a>
</td>
<td align="left" width="63%">
Reports that an item has been added to the Offline Files cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesevents-itemavailableoffline">ItemAvailableOffline</a>
</td>
<td align="left" width="63%">
Reports that an item in the Offline Files cache is now available for offline use should the remote copy become unavailable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesevents-itemdeletedfromcache">ItemDeletedFromCache</a>
</td>
<td align="left" width="63%">
Reports that an item has been removed from the Offline Files cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesevents-itemdisconnected">ItemDisconnected</a>
</td>
<td align="left" width="63%">
Reports that an item in the Offline Files cache has transitioned from online to offline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesevents-itemmodified">ItemModified</a>
</td>
<td align="left" width="63%">
Reports that an item in the Offline Files cache has been modified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesevents-itemnotavailableoffline">ItemNotAvailableOffline</a>
</td>
<td align="left" width="63%">
Reports that an item in the Offline Files cache is no longer available for offline use should the remote copy become unavailable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesevents-itemnotpinned">ItemNotPinned</a>
</td>
<td align="left" width="63%">
Reports that an item in the Offline Files cache is no longer pinned.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesevents-itempinned">ItemPinned</a>
</td>
<td align="left" width="63%">
Reports that an item in the Offline Files cache is now pinned and guaranteed to be available offline should the remote copy become unavailable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesevents-itemreconnected">ItemReconnected</a>
</td>
<td align="left" width="63%">
Reports that an item in the Offline Files cache has transitioned from offline to online.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesevents-itemrenamed">ItemRenamed</a>
</td>
<td align="left" width="63%">
Reports that an item in the Offline Files cache has been renamed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesevents-nettransportarrived">NetTransportArrived</a>
</td>
<td align="left" width="63%">
Reports that the Offline Files feature has detected the arrival of a network transport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesevents-nonettransports">NoNetTransports</a>
</td>
<td align="left" width="63%">
Reports that the Offline Files feature has detected that no network transports are available.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesevents-ping">Ping</a>
</td>
<td align="left" width="63%">
This event is delivered to all registered event subscribers on a periodic basis.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesevents-syncbegin">SyncBegin</a>
</td>
<td align="left" width="63%">
Reports that the Offline Files cache has begun a synchronize operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesevents-syncconflictrecadded">SyncConflictRecAdded</a>
</td>
<td align="left" width="63%">
Reports that a sync conflict has been detected and recorded in the sync conflict log.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesevents-syncconflictrecremoved">SyncConflictRecRemoved</a>
</td>
<td align="left" width="63%">
Reports that a sync conflict no longer exists and that its record has been removed from the sync conflict log.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesevents-syncconflictrecupdated">SyncConflictRecUpdated</a>
</td>
<td align="left" width="63%">
Reports that a sync conflict has been detected and that a record of the conflict was already present in the sync conflict log, and that the existing record has been updated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesevents-syncend">SyncEnd</a>
</td>
<td align="left" width="63%">
Reports that the Offline Files cache has ended a synchronize operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesevents-syncfileresult">SyncFileResult</a>
</td>
<td align="left" width="63%">
Reports the result of synchronizing a particular file.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/offlinefiles/offline-files-api-interfaces">Offline Files API Interfaces</a>