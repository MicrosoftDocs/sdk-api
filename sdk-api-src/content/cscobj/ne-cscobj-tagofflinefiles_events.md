---
UID: NE:cscobj.tagOFFLINEFILES_EVENTS
title: tagOFFLINEFILES_EVENTS
author: windows-sdk-content
description: Event identifier codes describing events to be received or excluded by an event sink.
old-location: of\offlinefiles_events.htm
tech.root: OfflineFiles
ms.assetid: 4ab65756-5985-4240-805d-2221db3d1459
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: OFFLINEFILES_EVENTS, OFFLINEFILES_EVENTS enumeration [Offline Files], OFFLINEFILES_EVENT_BACKGROUNDSYNCBEGIN, OFFLINEFILES_EVENT_BACKGROUNDSYNCEND, OFFLINEFILES_EVENT_CACHEEVICTBEGIN, OFFLINEFILES_EVENT_CACHEEVICTEND, OFFLINEFILES_EVENT_CACHEISCORRUPTED, OFFLINEFILES_EVENT_CACHEISFULL, OFFLINEFILES_EVENT_CACHEMOVED, OFFLINEFILES_EVENT_DATALOST, OFFLINEFILES_EVENT_ENABLED, OFFLINEFILES_EVENT_ENCRYPTIONCHANGED, OFFLINEFILES_EVENT_ITEMADDEDTOCACHE, OFFLINEFILES_EVENT_ITEMAVAILABLEOFFLINE, OFFLINEFILES_EVENT_ITEMDELETEDFROMCACHE, OFFLINEFILES_EVENT_ITEMDISCONNECTED, OFFLINEFILES_EVENT_ITEMMODIFIED, OFFLINEFILES_EVENT_ITEMNOTAVAILABLEOFFLINE, OFFLINEFILES_EVENT_ITEMNOTPINNED, OFFLINEFILES_EVENT_ITEMPINNED, OFFLINEFILES_EVENT_ITEMRECONNECTBEGIN, OFFLINEFILES_EVENT_ITEMRECONNECTED, OFFLINEFILES_EVENT_ITEMRECONNECTEND, OFFLINEFILES_EVENT_ITEMRENAMED, OFFLINEFILES_EVENT_NETTRANSPORTARRIVED, OFFLINEFILES_EVENT_NONETTRANSPORTS, OFFLINEFILES_EVENT_PING, OFFLINEFILES_EVENT_POLICYCHANGEDETECTED, OFFLINEFILES_EVENT_PREFERENCECHANGEDETECTED, OFFLINEFILES_EVENT_PREFETCHFILEBEGIN, OFFLINEFILES_EVENT_PREFETCHFILEEND, OFFLINEFILES_EVENT_SETTINGSCHANGESAPPLIED, OFFLINEFILES_EVENT_SYNCBEGIN, OFFLINEFILES_EVENT_SYNCCONFLICTRECADDED, OFFLINEFILES_EVENT_SYNCCONFLICTRECREMOVED, OFFLINEFILES_EVENT_SYNCCONFLICTRECUPDATED, OFFLINEFILES_EVENT_SYNCEND, OFFLINEFILES_EVENT_SYNCFILERESULT, OFFLINEFILES_EVENT_TRANSPARENTCACHEITEMNOTIFY, cscobj/OFFLINEFILES_EVENTS, cscobj/OFFLINEFILES_EVENT_BACKGROUNDSYNCBEGIN, cscobj/OFFLINEFILES_EVENT_BACKGROUNDSYNCEND, cscobj/OFFLINEFILES_EVENT_CACHEEVICTBEGIN, cscobj/OFFLINEFILES_EVENT_CACHEEVICTEND, cscobj/OFFLINEFILES_EVENT_CACHEISCORRUPTED, cscobj/OFFLINEFILES_EVENT_CACHEISFULL, cscobj/OFFLINEFILES_EVENT_CACHEMOVED, cscobj/OFFLINEFILES_EVENT_DATALOST, cscobj/OFFLINEFILES_EVENT_ENABLED, cscobj/OFFLINEFILES_EVENT_ENCRYPTIONCHANGED, cscobj/OFFLINEFILES_EVENT_ITEMADDEDTOCACHE, cscobj/OFFLINEFILES_EVENT_ITEMAVAILABLEOFFLINE, cscobj/OFFLINEFILES_EVENT_ITEMDELETEDFROMCACHE, cscobj/OFFLINEFILES_EVENT_ITEMDISCONNECTED, cscobj/OFFLINEFILES_EVENT_ITEMMODIFIED, cscobj/OFFLINEFILES_EVENT_ITEMNOTAVAILABLEOFFLINE, cscobj/OFFLINEFILES_EVENT_ITEMNOTPINNED, cscobj/OFFLINEFILES_EVENT_ITEMPINNED, cscobj/OFFLINEFILES_EVENT_ITEMRECONNECTBEGIN, cscobj/OFFLINEFILES_EVENT_ITEMRECONNECTED, cscobj/OFFLINEFILES_EVENT_ITEMRECONNECTEND, cscobj/OFFLINEFILES_EVENT_ITEMRENAMED, cscobj/OFFLINEFILES_EVENT_NETTRANSPORTARRIVED, cscobj/OFFLINEFILES_EVENT_NONETTRANSPORTS, cscobj/OFFLINEFILES_EVENT_PING, cscobj/OFFLINEFILES_EVENT_POLICYCHANGEDETECTED, cscobj/OFFLINEFILES_EVENT_PREFERENCECHANGEDETECTED, cscobj/OFFLINEFILES_EVENT_PREFETCHFILEBEGIN, cscobj/OFFLINEFILES_EVENT_PREFETCHFILEEND, cscobj/OFFLINEFILES_EVENT_SETTINGSCHANGESAPPLIED, cscobj/OFFLINEFILES_EVENT_SYNCBEGIN, cscobj/OFFLINEFILES_EVENT_SYNCCONFLICTRECADDED, cscobj/OFFLINEFILES_EVENT_SYNCCONFLICTRECREMOVED, cscobj/OFFLINEFILES_EVENT_SYNCCONFLICTRECUPDATED, cscobj/OFFLINEFILES_EVENT_SYNCEND, cscobj/OFFLINEFILES_EVENT_SYNCFILERESULT, cscobj/OFFLINEFILES_EVENT_TRANSPARENTCACHEITEMNOTIFY, of.offlinefiles_events, tagOFFLINEFILES_EVENTS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CscObj.h
api_name:
 - OFFLINEFILES_EVENTS
product: Windows
targetos: Windows
req.typenames: OFFLINEFILES_EVENTS
req.redist: 
---

# tagOFFLINEFILES_EVENTS enumeration


## -description


Event identifier codes describing events to be received or excluded by an event sink. Used with the <a href="https://msdn.microsoft.com/en-us/library/Bb530535(v=VS.85).aspx">IOfflineFilesEventsFilter::GetIncludedEvents</a> and <a href="https://msdn.microsoft.com/en-us/library/Bb530533(v=VS.85).aspx">IOfflineFilesEventsFilter::GetExcludedEvents</a> methods.


## -enum-fields




### -field OFFLINEFILES_EVENT_CACHEMOVED

This value is reserved for future use.


### -field OFFLINEFILES_EVENT_CACHEISFULL

This value is reserved for future use.


### -field OFFLINEFILES_EVENT_CACHEISCORRUPTED

This value is reserved for future use.


### -field OFFLINEFILES_EVENT_ENABLED

This value is reserved for future use.


### -field OFFLINEFILES_EVENT_ENCRYPTIONCHANGED

This value is reserved for future use.


### -field OFFLINEFILES_EVENT_SYNCBEGIN

Represents the <a href="https://msdn.microsoft.com/en-us/library/Bb530559(v=VS.85).aspx">IOfflineFilesEvents::SyncBegin</a> event method.


### -field OFFLINEFILES_EVENT_SYNCFILERESULT

Represents the <a href="https://msdn.microsoft.com/en-us/library/Bb530564(v=VS.85).aspx">IOfflineFilesEvents::SyncFileResult</a> event method.


### -field OFFLINEFILES_EVENT_SYNCCONFLICTRECADDED

Represents the <a href="https://msdn.microsoft.com/en-us/library/Bb530560(v=VS.85).aspx">IOfflineFilesEvents::SyncConflictRecAdded</a> event method.


### -field OFFLINEFILES_EVENT_SYNCCONFLICTRECUPDATED

Represents the <a href="https://msdn.microsoft.com/en-us/library/Bb530562(v=VS.85).aspx">IOfflineFilesEvents::SyncConflictRecUpdated</a> event method.


### -field OFFLINEFILES_EVENT_SYNCCONFLICTRECREMOVED

Represents the <a href="https://msdn.microsoft.com/en-us/library/Bb530561(v=VS.85).aspx">IOfflineFilesEvents::SyncConflictRecRemoved</a> event method.


### -field OFFLINEFILES_EVENT_SYNCEND

Represents the <a href="https://msdn.microsoft.com/en-us/library/Bb530563(v=VS.85).aspx">IOfflineFilesEvents::SyncEnd</a> event method.


### -field OFFLINEFILES_EVENT_BACKGROUNDSYNCBEGIN

Represents the <a href="https://msdn.microsoft.com/en-us/library/Bb530522(v=VS.85).aspx">IOfflineFilesEvents2::BackgroundSyncBegin</a> event method.


### -field OFFLINEFILES_EVENT_BACKGROUNDSYNCEND

Represents the <a href="https://msdn.microsoft.com/en-us/library/Bb530524(v=VS.85).aspx">IOfflineFilesEvents2::BackgroundSyncEnd</a> event method.


### -field OFFLINEFILES_EVENT_NETTRANSPORTARRIVED

Represents the <a href="https://msdn.microsoft.com/en-us/library/Bb530556(v=VS.85).aspx">IOfflineFilesEvents::NetTransportArrived</a> event method.


### -field OFFLINEFILES_EVENT_NONETTRANSPORTS

Represents the <a href="https://msdn.microsoft.com/en-us/library/Bb530557(v=VS.85).aspx">IOfflineFilesEvents::NoNetTransports</a> event method.


### -field OFFLINEFILES_EVENT_ITEMDISCONNECTED

Represents the <a href="https://msdn.microsoft.com/en-us/library/Bb530548(v=VS.85).aspx">IOfflineFilesEvents::ItemDisconnected</a> event method.


### -field OFFLINEFILES_EVENT_ITEMRECONNECTED

Represents the <a href="https://msdn.microsoft.com/en-us/library/Bb530553(v=VS.85).aspx">IOfflineFilesEvents::ItemReconnected</a> event method.


### -field OFFLINEFILES_EVENT_ITEMAVAILABLEOFFLINE

Represents the <a href="https://msdn.microsoft.com/en-us/library/Bb530546(v=VS.85).aspx">IOfflineFilesEvents::ItemAvailableOffline</a> event method.


### -field OFFLINEFILES_EVENT_ITEMNOTAVAILABLEOFFLINE

Represents the <a href="https://msdn.microsoft.com/en-us/library/Bb530550(v=VS.85).aspx">IOfflineFilesEvents::ItemNotAvailableOffline</a> event method.


### -field OFFLINEFILES_EVENT_ITEMPINNED

Represents the <a href="https://msdn.microsoft.com/en-us/library/Bb530552(v=VS.85).aspx">IOfflineFilesEvents::ItemPinned</a> event method.


### -field OFFLINEFILES_EVENT_ITEMNOTPINNED

Represents the <a href="https://msdn.microsoft.com/en-us/library/Bb530551(v=VS.85).aspx">IOfflineFilesEvents::ItemNotPinned</a> event method.


### -field OFFLINEFILES_EVENT_ITEMMODIFIED

Represents the <a href="https://msdn.microsoft.com/en-us/library/Bb530549(v=VS.85).aspx">IOfflineFilesEvents::ItemModified</a> event method.


### -field OFFLINEFILES_EVENT_ITEMADDEDTOCACHE

Represents the <a href="https://msdn.microsoft.com/en-us/library/Bb530545(v=VS.85).aspx">IOfflineFilesEvents::ItemAddedToCache</a> event method.


### -field OFFLINEFILES_EVENT_ITEMDELETEDFROMCACHE

Represents the <a href="https://msdn.microsoft.com/en-us/library/Bb530547(v=VS.85).aspx">IOfflineFilesEvents::ItemDeletedFromCache</a> event method.


### -field OFFLINEFILES_EVENT_ITEMRENAMED

Represents the <a href="https://msdn.microsoft.com/en-us/library/Bb530554(v=VS.85).aspx">IOfflineFilesEvents::ItemRenamed</a> event method.


### -field OFFLINEFILES_EVENT_DATALOST

Represents the <a href="https://msdn.microsoft.com/en-us/library/Bb530541(v=VS.85).aspx">IOfflineFilesEvents::DataLost</a> event method.


### -field OFFLINEFILES_EVENT_PING

Represents the <a href="https://msdn.microsoft.com/en-us/library/Bb530558(v=VS.85).aspx">IOfflineFilesEvents::Ping</a> event method.


### -field OFFLINEFILES_EVENT_ITEMRECONNECTBEGIN

Represents the <a href="https://msdn.microsoft.com/en-us/library/Bb530527(v=VS.85).aspx">IOfflineFilesEvents2::ItemReconnectBegin</a> event method.


### -field OFFLINEFILES_EVENT_ITEMRECONNECTEND

Represents the <a href="https://msdn.microsoft.com/en-us/library/Bb530528(v=VS.85).aspx">IOfflineFilesEvents2::ItemReconnectEnd</a> event method.


### -field OFFLINEFILES_EVENT_CACHEEVICTBEGIN

This value is reserved for future use.


### -field OFFLINEFILES_EVENT_CACHEEVICTEND

This value is reserved for future use.


### -field OFFLINEFILES_EVENT_POLICYCHANGEDETECTED

Represents the <a href="https://msdn.microsoft.com/en-us/library/Bb530529(v=VS.85).aspx">IOfflineFilesEvents2::PolicyChangeDetected</a> event method.


### -field OFFLINEFILES_EVENT_PREFERENCECHANGEDETECTED

Represents the <a href="https://msdn.microsoft.com/en-us/library/Bb530530(v=VS.85).aspx">IOfflineFilesEvents2::PreferenceChangeDetected</a> event method.


### -field OFFLINEFILES_EVENT_SETTINGSCHANGESAPPLIED

Represents the <a href="https://msdn.microsoft.com/en-us/library/Bb530531(v=VS.85).aspx">IOfflineFilesEvents2::SettingsChangesApplied</a> event method.


### -field OFFLINEFILES_EVENT_TRANSPARENTCACHEITEMNOTIFY

Represents the <a href="https://msdn.microsoft.com/en-us/library/Dd442648(v=VS.85).aspx">IOfflineFilesEvents3::TransparentCacheItemNotify</a> event method.

<b>Windows Server 2008 and Windows Vista:  </b>This value is not supported before Windows Server 2008 R2 and Windows 7.


### -field OFFLINEFILES_EVENT_PREFETCHFILEBEGIN

Represents the <a href="https://msdn.microsoft.com/en-us/library/Dd442646(v=VS.85).aspx">IOfflineFilesEvents3::PrefetchFileBegin</a> event method.

<b>Windows Server 2008 and Windows Vista:  </b>This value is not supported before Windows Server 2008 R2 and Windows 7.


### -field OFFLINEFILES_EVENT_PREFETCHFILEEND

Represents the <a href="https://msdn.microsoft.com/en-us/library/Dd442647(v=VS.85).aspx">IOfflineFilesEvents3::PrefetchFileEnd</a> event method.

<b>Windows Server 2008 and Windows Vista:  </b>This value is not supported before Windows Server 2008 R2 and Windows 7.


### -field OFFLINEFILES_EVENT_PREFETCHCLOSEHANDLEBEGIN


### -field OFFLINEFILES_EVENT_PREFETCHCLOSEHANDLEEND


### -field OFFLINEFILES_NUM_EVENTS




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb530533(v=VS.85).aspx">IOfflineFilesEventsFilter::GetExcludedEvents</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb530535(v=VS.85).aspx">IOfflineFilesEventsFilter::GetIncludedEvents</a>
 

 

