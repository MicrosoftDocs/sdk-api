---
UID: NN:cscobj.IOfflineFilesEvents
title: IOfflineFilesEvents
author: windows-sdk-content
description: Used to report significant events associated with Offline Files.
old-location: of\iofflinefilesevents.htm
tech.root: OfflineFiles
ms.assetid: c0bd0033-e5e1-4d21-8d98-eb937acdd6cf
ms.author: windowssdkdev
ms.date: 09/26/2018
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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IOfflineFilesEvents</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Bb530537(v=VS.85).aspx">CacheIsCorrupted</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530538(v=VS.85).aspx">CacheIsFull</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530540(v=VS.85).aspx">CacheMoved</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530541(v=VS.85).aspx">DataLost</a>
</td>
<td align="left" width="63%">
Reports that one or more events destined for this event sink have been lost and will not be delivered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530542(v=VS.85).aspx">Enabled</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530544(v=VS.85).aspx">EncryptionChanged</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530545(v=VS.85).aspx">ItemAddedToCache</a>
</td>
<td align="left" width="63%">
Reports that an item has been added to the Offline Files cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530546(v=VS.85).aspx">ItemAvailableOffline</a>
</td>
<td align="left" width="63%">
Reports that an item in the Offline Files cache is now available for offline use should the remote copy become unavailable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530547(v=VS.85).aspx">ItemDeletedFromCache</a>
</td>
<td align="left" width="63%">
Reports that an item has been removed from the Offline Files cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530548(v=VS.85).aspx">ItemDisconnected</a>
</td>
<td align="left" width="63%">
Reports that an item in the Offline Files cache has transitioned from online to offline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530549(v=VS.85).aspx">ItemModified</a>
</td>
<td align="left" width="63%">
Reports that an item in the Offline Files cache has been modified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530550(v=VS.85).aspx">ItemNotAvailableOffline</a>
</td>
<td align="left" width="63%">
Reports that an item in the Offline Files cache is no longer available for offline use should the remote copy become unavailable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530551(v=VS.85).aspx">ItemNotPinned</a>
</td>
<td align="left" width="63%">
Reports that an item in the Offline Files cache is no longer pinned.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530552(v=VS.85).aspx">ItemPinned</a>
</td>
<td align="left" width="63%">
Reports that an item in the Offline Files cache is now pinned and guaranteed to be available offline should the remote copy become unavailable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530553(v=VS.85).aspx">ItemReconnected</a>
</td>
<td align="left" width="63%">
Reports that an item in the Offline Files cache has transitioned from offline to online.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530554(v=VS.85).aspx">ItemRenamed</a>
</td>
<td align="left" width="63%">
Reports that an item in the Offline Files cache has been renamed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530556(v=VS.85).aspx">NetTransportArrived</a>
</td>
<td align="left" width="63%">
Reports that the Offline Files feature has detected the arrival of a network transport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530557(v=VS.85).aspx">NoNetTransports</a>
</td>
<td align="left" width="63%">
Reports that the Offline Files feature has detected that no network transports are available.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530558(v=VS.85).aspx">Ping</a>
</td>
<td align="left" width="63%">
This event is delivered to all registered event subscribers on a periodic basis.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530559(v=VS.85).aspx">SyncBegin</a>
</td>
<td align="left" width="63%">
Reports that the Offline Files cache has begun a synchronize operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530560(v=VS.85).aspx">SyncConflictRecAdded</a>
</td>
<td align="left" width="63%">
Reports that a sync conflict has been detected and recorded in the sync conflict log.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530561(v=VS.85).aspx">SyncConflictRecRemoved</a>
</td>
<td align="left" width="63%">
Reports that a sync conflict no longer exists and that its record has been removed from the sync conflict log.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530562(v=VS.85).aspx">SyncConflictRecUpdated</a>
</td>
<td align="left" width="63%">
Reports that a sync conflict has been detected and that a record of the conflict was already present in the sync conflict log, and that the existing record has been updated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530563(v=VS.85).aspx">SyncEnd</a>
</td>
<td align="left" width="63%">
Reports that the Offline Files cache has ended a synchronize operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530564(v=VS.85).aspx">SyncFileResult</a>
</td>
<td align="left" width="63%">
Reports the result of synchronizing a particular file.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb530659(v=VS.85).aspx">Offline Files API Interfaces</a>
 

 

