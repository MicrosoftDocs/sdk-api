---
UID: NF:cscobj.IOfflineFilesEvents.ItemAddedToCache
title: IOfflineFilesEvents::ItemAddedToCache
author: windows-sdk-content
description: Reports that an item has been added to the Offline Files cache.
old-location: of\iofflinefilesevents_itemaddedtocache.htm
old-project: offlinefiles
ms.assetid: 7ab04b07-f72a-4a04-a470-4b85c21005c0
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IOfflineFilesEvents interface [Offline Files],ItemAddedToCache method, IOfflineFilesEvents.ItemAddedToCache, IOfflineFilesEvents::ItemAddedToCache, ItemAddedToCache, ItemAddedToCache method [Offline Files], ItemAddedToCache method [Offline Files],IOfflineFilesEvents interface, cscobj/IOfflineFilesEvents::ItemAddedToCache, of.iofflinefilesevents_itemaddedtocache
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: OFFLINEFILES_SYNC_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesEvents.ItemAddedToCache
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IOfflineFilesEvents::ItemAddedToCache


## -description


Reports that an item has been added to the Offline Files cache.


## -parameters




### -param pszPath [in]

The item's UNC path string.


### -param ItemType [in]

An <a href="https://msdn.microsoft.com/cf8bb079-d691-4b37-b408-d1af1746ed37">OFFLINEFILES_ITEM_TYPE</a> enumeration value that indicates the type of the item.


## -returns



The return value is ignored.




## -remarks



Note that addition to the cache does not mean that the item is available for offline use.  It may still be sparsely cached.  When the item is available for offline use, the <a href="https://msdn.microsoft.com/6c629ede-00ee-4f5e-9f75-022e3c5b3957">ItemAvailableOffline</a> event will be sent.




## -see-also




<a href="https://msdn.microsoft.com/c0bd0033-e5e1-4d21-8d98-eb937acdd6cf">IOfflineFilesEvents</a>
 

 

