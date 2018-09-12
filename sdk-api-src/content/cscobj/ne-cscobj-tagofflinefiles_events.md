---
UID: NE:cscobj.tagOFFLINEFILES_EVENTS
title: tagOFFLINEFILES_EVENTS
author: windows-sdk-content
description: Event identifier codes describing events to be received or excluded by an event sink.
old-location: of\offlinefiles_events.htm
tech.root: offlinefiles
ms.assetid: 4ab65756-5985-4240-805d-2221db3d1459
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: OFFLINEFILES_EVENTS, OFFLINEFILES_EVENTS enumeration [Offline Files], OFFLINEFILES_EVENT_BACKGROUNDSYNCBEGIN, OFFLINEFILES_EVENT_BACKGROUNDSYNCEND, OFFLINEFILES_EVENT_CACHEEVICTBEGIN, OFFLINEFILES_EVENT_CACHEEVICTEND, OFFLINEFILES_EVENT_CACHEISCORRUPTED, OFFLINEFILES_EVENT_CACHEISFULL, OFFLINEFILES_EVENT_CACHEMOVED, OFFLINEFILES_EVENT_DATALOST, OFFLINEFILES_EVENT_ENABLED, OFFLINEFILES_EVENT_ENCRYPTIONCHANGED, OFFLINEFILES_EVENT_ITEMADDEDTOCACHE, OFFLINEFILES_EVENT_ITEMAVAILABLEOFFLINE, OFFLINEFILES_EVENT_ITEMDELETEDFROMCACHE, OFFLINEFILES_EVENT_ITEMDISCONNECTED, OFFLINEFILES_EVENT_ITEMMODIFIED, OFFLINEFILES_EVENT_ITEMNOTAVAILABLEOFFLINE, OFFLINEFILES_EVENT_ITEMNOTPINNED, OFFLINEFILES_EVENT_ITEMPINNED, OFFLINEFILES_EVENT_ITEMRECONNECTBEGIN, OFFLINEFILES_EVENT_ITEMRECONNECTED, OFFLINEFILES_EVENT_ITEMRECONNECTEND, OFFLINEFILES_EVENT_ITEMRENAMED, OFFLINEFILES_EVENT_NETTRANSPORTARRIVED, OFFLINEFILES_EVENT_NONETTRANSPORTS, OFFLINEFILES_EVENT_PING, OFFLINEFILES_EVENT_POLICYCHANGEDETECTED, OFFLINEFILES_EVENT_PREFERENCECHANGEDETECTED, OFFLINEFILES_EVENT_PREFETCHFILEBEGIN, OFFLINEFILES_EVENT_PREFETCHFILEEND, OFFLINEFILES_EVENT_SETTINGSCHANGESAPPLIED, OFFLINEFILES_EVENT_SYNCBEGIN, OFFLINEFILES_EVENT_SYNCCONFLICTRECADDED, OFFLINEFILES_EVENT_SYNCCONFLICTRECREMOVED, OFFLINEFILES_EVENT_SYNCCONFLICTRECUPDATED, OFFLINEFILES_EVENT_SYNCEND, OFFLINEFILES_EVENT_SYNCFILERESULT, OFFLINEFILES_EVENT_TRANSPARENTCACHEITEMNOTIFY, cscobj/OFFLINEFILES_EVENTS, cscobj/OFFLINEFILES_EVENT_BACKGROUNDSYNCBEGIN, cscobj/OFFLINEFILES_EVENT_BACKGROUNDSYNCEND, cscobj/OFFLINEFILES_EVENT_CACHEEVICTBEGIN, cscobj/OFFLINEFILES_EVENT_CACHEEVICTEND, cscobj/OFFLINEFILES_EVENT_CACHEISCORRUPTED, cscobj/OFFLINEFILES_EVENT_CACHEISFULL, cscobj/OFFLINEFILES_EVENT_CACHEMOVED, cscobj/OFFLINEFILES_EVENT_DATALOST, cscobj/OFFLINEFILES_EVENT_ENABLED, cscobj/OFFLINEFILES_EVENT_ENCRYPTIONCHANGED, cscobj/OFFLINEFILES_EVENT_ITEMADDEDTOCACHE, cscobj/OFFLINEFILES_EVENT_ITEMAVAILABLEOFFLINE, cscobj/OFFLINEFILES_EVENT_ITEMDELETEDFROMCACHE, cscobj/OFFLINEFILES_EVENT_ITEMDISCONNECTED, cscobj/OFFLINEFILES_EVENT_ITEMMODIFIED, cscobj/OFFLINEFILES_EVENT_ITEMNOTAVAILABLEOFFLINE, cscobj/OFFLINEFILES_EVENT_ITEMNOTPINNED, cscobj/OFFLINEFILES_EVENT_ITEMPINNED, cscobj/OFFLINEFILES_EVENT_ITEMRECONNECTBEGIN, cscobj/OFFLINEFILES_EVENT_ITEMRECONNECTED, cscobj/OFFLINEFILES_EVENT_ITEMRECONNECTEND, cscobj/OFFLINEFILES_EVENT_ITEMRENAMED, cscobj/OFFLINEFILES_EVENT_NETTRANSPORTARRIVED, cscobj/OFFLINEFILES_EVENT_NONETTRANSPORTS, cscobj/OFFLINEFILES_EVENT_PING, cscobj/OFFLINEFILES_EVENT_POLICYCHANGEDETECTED, cscobj/OFFLINEFILES_EVENT_PREFERENCECHANGEDETECTED, cscobj/OFFLINEFILES_EVENT_PREFETCHFILEBEGIN, cscobj/OFFLINEFILES_EVENT_PREFETCHFILEEND, cscobj/OFFLINEFILES_EVENT_SETTINGSCHANGESAPPLIED, cscobj/OFFLINEFILES_EVENT_SYNCBEGIN, cscobj/OFFLINEFILES_EVENT_SYNCCONFLICTRECADDED, cscobj/OFFLINEFILES_EVENT_SYNCCONFLICTRECREMOVED, cscobj/OFFLINEFILES_EVENT_SYNCCONFLICTRECUPDATED, cscobj/OFFLINEFILES_EVENT_SYNCEND, cscobj/OFFLINEFILES_EVENT_SYNCFILERESULT, cscobj/OFFLINEFILES_EVENT_TRANSPARENTCACHEITEMNOTIFY, of.offlinefiles_events, tagOFFLINEFILES_EVENTS
ms.prod: windows
ms.technology: windows-sdk
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


Event identifier codes describing events to be received or excluded by an event sink. Used with the <a href="https://msdn.microsoft.com/ecb10da3-7566-43f7-8349-f94e59e12907">IOfflineFilesEventsFilter::GetIncludedEvents</a> and <a href="https://msdn.microsoft.com/40e388b2-b051-4b0a-b96e-7a73b521758e">IOfflineFilesEventsFilter::GetExcludedEvents</a> methods.


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

Represents the <a href="https://msdn.microsoft.com/ba09be0a-52bc-4715-9756-383954277a31">IOfflineFilesEvents::SyncBegin</a> event method.


### -field OFFLINEFILES_EVENT_SYNCFILERESULT

Represents the <a href="https://msdn.microsoft.com/3770e966-7481-449e-9b57-44a7329d26db">IOfflineFilesEvents::SyncFileResult</a> event method.


### -field OFFLINEFILES_EVENT_SYNCCONFLICTRECADDED

Represents the <a href="https://msdn.microsoft.com/693306de-d968-4857-8221-965b2f271aae">IOfflineFilesEvents::SyncConflictRecAdded</a> event method.


### -field OFFLINEFILES_EVENT_SYNCCONFLICTRECUPDATED

Represents the <a href="https://msdn.microsoft.com/adf13e95-bcb0-4f84-bbb9-9648f90f3be8">IOfflineFilesEvents::SyncConflictRecUpdated</a> event method.


### -field OFFLINEFILES_EVENT_SYNCCONFLICTRECREMOVED

Represents the <a href="https://msdn.microsoft.com/ccdd7b74-3e00-4a3d-9632-eac48d790f23">IOfflineFilesEvents::SyncConflictRecRemoved</a> event method.


### -field OFFLINEFILES_EVENT_SYNCEND

Represents the <a href="https://msdn.microsoft.com/2b4b32b9-7268-4f79-8eac-640a6c62b0c1">IOfflineFilesEvents::SyncEnd</a> event method.


### -field OFFLINEFILES_EVENT_BACKGROUNDSYNCBEGIN

Represents the <a href="https://msdn.microsoft.com/84b71228-904a-4042-8d13-422ae77f7ba5">IOfflineFilesEvents2::BackgroundSyncBegin</a> event method.


### -field OFFLINEFILES_EVENT_BACKGROUNDSYNCEND

Represents the <a href="https://msdn.microsoft.com/d41a2152-8100-47a7-a994-a0fe9fae4dc4">IOfflineFilesEvents2::BackgroundSyncEnd</a> event method.


### -field OFFLINEFILES_EVENT_NETTRANSPORTARRIVED

Represents the <a href="https://msdn.microsoft.com/ac44010b-b14f-41d7-89f7-6f7822ed2a5d">IOfflineFilesEvents::NetTransportArrived</a> event method.


### -field OFFLINEFILES_EVENT_NONETTRANSPORTS

Represents the <a href="https://msdn.microsoft.com/4970acd4-b99d-4d7a-a0bc-04c10a4423b8">IOfflineFilesEvents::NoNetTransports</a> event method.


### -field OFFLINEFILES_EVENT_ITEMDISCONNECTED

Represents the <a href="https://msdn.microsoft.com/b0f9d873-cda5-4805-bb5e-d23d47b53f1d">IOfflineFilesEvents::ItemDisconnected</a> event method.


### -field OFFLINEFILES_EVENT_ITEMRECONNECTED

Represents the <a href="https://msdn.microsoft.com/beafae9d-3ef8-401f-8ab6-79d2ae3366a4">IOfflineFilesEvents::ItemReconnected</a> event method.


### -field OFFLINEFILES_EVENT_ITEMAVAILABLEOFFLINE

Represents the <a href="https://msdn.microsoft.com/6c629ede-00ee-4f5e-9f75-022e3c5b3957">IOfflineFilesEvents::ItemAvailableOffline</a> event method.


### -field OFFLINEFILES_EVENT_ITEMNOTAVAILABLEOFFLINE

Represents the <a href="https://msdn.microsoft.com/868938fd-9da2-45fd-a00e-5dda85b4fd61">IOfflineFilesEvents::ItemNotAvailableOffline</a> event method.


### -field OFFLINEFILES_EVENT_ITEMPINNED

Represents the <a href="https://msdn.microsoft.com/cf298e4e-97c8-4f6f-b6f5-0bd0d9435599">IOfflineFilesEvents::ItemPinned</a> event method.


### -field OFFLINEFILES_EVENT_ITEMNOTPINNED

Represents the <a href="https://msdn.microsoft.com/cefd7408-9e98-48a4-ad43-0bdef9da1c95">IOfflineFilesEvents::ItemNotPinned</a> event method.


### -field OFFLINEFILES_EVENT_ITEMMODIFIED

Represents the <a href="https://msdn.microsoft.com/e689b111-d6d1-436e-b468-570e575a5170">IOfflineFilesEvents::ItemModified</a> event method.


### -field OFFLINEFILES_EVENT_ITEMADDEDTOCACHE

Represents the <a href="https://msdn.microsoft.com/7ab04b07-f72a-4a04-a470-4b85c21005c0">IOfflineFilesEvents::ItemAddedToCache</a> event method.


### -field OFFLINEFILES_EVENT_ITEMDELETEDFROMCACHE

Represents the <a href="https://msdn.microsoft.com/358b358a-65cc-4f37-8beb-be492b83c222">IOfflineFilesEvents::ItemDeletedFromCache</a> event method.


### -field OFFLINEFILES_EVENT_ITEMRENAMED

Represents the <a href="https://msdn.microsoft.com/f1a678dd-9a02-41da-90d4-930c0d366a36">IOfflineFilesEvents::ItemRenamed</a> event method.


### -field OFFLINEFILES_EVENT_DATALOST

Represents the <a href="https://msdn.microsoft.com/da0414dd-2acb-48d9-ac84-66bb1f7ccbef">IOfflineFilesEvents::DataLost</a> event method.


### -field OFFLINEFILES_EVENT_PING

Represents the <a href="https://msdn.microsoft.com/edde2f37-f082-4382-8908-181bc42d30ef">IOfflineFilesEvents::Ping</a> event method.


### -field OFFLINEFILES_EVENT_ITEMRECONNECTBEGIN

Represents the <a href="https://msdn.microsoft.com/7b0d112d-17be-481a-8793-2b57506ec7b2">IOfflineFilesEvents2::ItemReconnectBegin</a> event method.


### -field OFFLINEFILES_EVENT_ITEMRECONNECTEND

Represents the <a href="https://msdn.microsoft.com/929d6556-69cb-4863-a665-236603fcd88b">IOfflineFilesEvents2::ItemReconnectEnd</a> event method.


### -field OFFLINEFILES_EVENT_CACHEEVICTBEGIN

This value is reserved for future use.


### -field OFFLINEFILES_EVENT_CACHEEVICTEND

This value is reserved for future use.


### -field OFFLINEFILES_EVENT_POLICYCHANGEDETECTED

Represents the <a href="https://msdn.microsoft.com/1009c67a-09f4-40ea-8aa9-fb42f1ab54ff">IOfflineFilesEvents2::PolicyChangeDetected</a> event method.


### -field OFFLINEFILES_EVENT_PREFERENCECHANGEDETECTED

Represents the <a href="https://msdn.microsoft.com/c947d9e5-2712-4dbd-8806-79a8bf0f4cc9">IOfflineFilesEvents2::PreferenceChangeDetected</a> event method.


### -field OFFLINEFILES_EVENT_SETTINGSCHANGESAPPLIED

Represents the <a href="https://msdn.microsoft.com/af59c8ac-ecd4-48e7-9ebb-8802e7d6ffef">IOfflineFilesEvents2::SettingsChangesApplied</a> event method.


### -field OFFLINEFILES_EVENT_TRANSPARENTCACHEITEMNOTIFY

Represents the <a href="https://msdn.microsoft.com/59bd7a71-0189-4c4d-a737-e6a3f09a533d">IOfflineFilesEvents3::TransparentCacheItemNotify</a> event method.

<b>Windows Server 2008 and Windows Vista:  </b>This value is not supported before Windows Server 2008 R2 and Windows 7.


### -field OFFLINEFILES_EVENT_PREFETCHFILEBEGIN

Represents the <a href="https://msdn.microsoft.com/b65354ed-dc4b-491c-9672-2f5fa91093bd">IOfflineFilesEvents3::PrefetchFileBegin</a> event method.

<b>Windows Server 2008 and Windows Vista:  </b>This value is not supported before Windows Server 2008 R2 and Windows 7.


### -field OFFLINEFILES_EVENT_PREFETCHFILEEND

Represents the <a href="https://msdn.microsoft.com/d5370d39-dd66-49c1-8774-cf335aa88e96">IOfflineFilesEvents3::PrefetchFileEnd</a> event method.

<b>Windows Server 2008 and Windows Vista:  </b>This value is not supported before Windows Server 2008 R2 and Windows 7.


### -field OFFLINEFILES_EVENT_PREFETCHCLOSEHANDLEBEGIN


### -field OFFLINEFILES_EVENT_PREFETCHCLOSEHANDLEEND


### -field OFFLINEFILES_NUM_EVENTS




## -see-also




<a href="https://msdn.microsoft.com/40e388b2-b051-4b0a-b96e-7a73b521758e">IOfflineFilesEventsFilter::GetExcludedEvents</a>



<a href="https://msdn.microsoft.com/ecb10da3-7566-43f7-8349-f94e59e12907">IOfflineFilesEventsFilter::GetIncludedEvents</a>
 

 

