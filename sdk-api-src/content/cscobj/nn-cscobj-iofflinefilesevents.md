---
UID: NN:cscobj.IOfflineFilesEvents
title: IOfflineFilesEvents
author: windows-sdk-content
description: Used to report significant events associated with Offline Files.
old-location: of\iofflinefilesevents.htm
tech.root: OfflineFiles
ms.assetid: c0bd0033-e5e1-4d21-8d98-eb937acdd6cf
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IOfflineFilesEvents, IOfflineFilesEvents interface [Offline Files], IOfflineFilesEvents interface [Offline Files],described, cscobj/IOfflineFilesEvents, of.iofflinefilesevents
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOfflineFilesEvents interface


## -description


 Used to report significant events associated with Offline Files.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IOfflineFilesEvents</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/d76d9af4-bfc4-4584-b014-31a62a2894cf">CacheIsCorrupted</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/535998f6-846b-4075-9504-a8d3e90a73b9">CacheIsFull</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/73d9bb7b-4844-4d7c-9e50-8d63727f5309">CacheMoved</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da0414dd-2acb-48d9-ac84-66bb1f7ccbef">DataLost</a>
</td>
<td align="left" width="63%">
Reports that one or more events destined for this event sink have been lost and will not be delivered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/47db9318-2418-4e6c-aac0-75b0b498c7e6">Enabled</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0cf93bed-e1b3-428f-a332-d50b575749f7">EncryptionChanged</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7ab04b07-f72a-4a04-a470-4b85c21005c0">ItemAddedToCache</a>
</td>
<td align="left" width="63%">
Reports that an item has been added to the Offline Files cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6c629ede-00ee-4f5e-9f75-022e3c5b3957">ItemAvailableOffline</a>
</td>
<td align="left" width="63%">
Reports that an item in the Offline Files cache is now available for offline use should the remote copy become unavailable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/358b358a-65cc-4f37-8beb-be492b83c222">ItemDeletedFromCache</a>
</td>
<td align="left" width="63%">
Reports that an item has been removed from the Offline Files cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b0f9d873-cda5-4805-bb5e-d23d47b53f1d">ItemDisconnected</a>
</td>
<td align="left" width="63%">
Reports that an item in the Offline Files cache has transitioned from online to offline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e689b111-d6d1-436e-b468-570e575a5170">ItemModified</a>
</td>
<td align="left" width="63%">
Reports that an item in the Offline Files cache has been modified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/868938fd-9da2-45fd-a00e-5dda85b4fd61">ItemNotAvailableOffline</a>
</td>
<td align="left" width="63%">
Reports that an item in the Offline Files cache is no longer available for offline use should the remote copy become unavailable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cefd7408-9e98-48a4-ad43-0bdef9da1c95">ItemNotPinned</a>
</td>
<td align="left" width="63%">
Reports that an item in the Offline Files cache is no longer pinned.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cf298e4e-97c8-4f6f-b6f5-0bd0d9435599">ItemPinned</a>
</td>
<td align="left" width="63%">
Reports that an item in the Offline Files cache is now pinned and guaranteed to be available offline should the remote copy become unavailable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/beafae9d-3ef8-401f-8ab6-79d2ae3366a4">ItemReconnected</a>
</td>
<td align="left" width="63%">
Reports that an item in the Offline Files cache has transitioned from offline to online.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f1a678dd-9a02-41da-90d4-930c0d366a36">ItemRenamed</a>
</td>
<td align="left" width="63%">
Reports that an item in the Offline Files cache has been renamed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ac44010b-b14f-41d7-89f7-6f7822ed2a5d">NetTransportArrived</a>
</td>
<td align="left" width="63%">
Reports that the Offline Files feature has detected the arrival of a network transport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4970acd4-b99d-4d7a-a0bc-04c10a4423b8">NoNetTransports</a>
</td>
<td align="left" width="63%">
Reports that the Offline Files feature has detected that no network transports are available.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/edde2f37-f082-4382-8908-181bc42d30ef">Ping</a>
</td>
<td align="left" width="63%">
This event is delivered to all registered event subscribers on a periodic basis.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ba09be0a-52bc-4715-9756-383954277a31">SyncBegin</a>
</td>
<td align="left" width="63%">
Reports that the Offline Files cache has begun a synchronize operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/693306de-d968-4857-8221-965b2f271aae">SyncConflictRecAdded</a>
</td>
<td align="left" width="63%">
Reports that a sync conflict has been detected and recorded in the sync conflict log.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ccdd7b74-3e00-4a3d-9632-eac48d790f23">SyncConflictRecRemoved</a>
</td>
<td align="left" width="63%">
Reports that a sync conflict no longer exists and that its record has been removed from the sync conflict log.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/adf13e95-bcb0-4f84-bbb9-9648f90f3be8">SyncConflictRecUpdated</a>
</td>
<td align="left" width="63%">
Reports that a sync conflict has been detected and that a record of the conflict was already present in the sync conflict log, and that the existing record has been updated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b4b32b9-7268-4f79-8eac-640a6c62b0c1">SyncEnd</a>
</td>
<td align="left" width="63%">
Reports that the Offline Files cache has ended a synchronize operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3770e966-7481-449e-9b57-44a7329d26db">SyncFileResult</a>
</td>
<td align="left" width="63%">
Reports the result of synchronizing a particular file.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/9dea396f-ab71-4b2e-b5d3-776c16614f26">Offline Files API Interfaces</a>
 

 

