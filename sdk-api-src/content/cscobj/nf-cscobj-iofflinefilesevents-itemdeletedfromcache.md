---
UID: NF:cscobj.IOfflineFilesEvents.ItemDeletedFromCache
title: IOfflineFilesEvents::ItemDeletedFromCache
author: windows-driver-content
description: Reports that an item has been removed from the Offline Files cache.
old-location: of\iofflinefilesevents_itemdeletedfromcache.htm
old-project: OfflineFiles
ms.assetid: 358b358a-65cc-4f37-8beb-be492b83c222
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IOfflineFilesEvents interface [Offline Files],ItemDeletedFromCache method, IOfflineFilesEvents.ItemDeletedFromCache, IOfflineFilesEvents::ItemDeletedFromCache, ItemDeletedFromCache, ItemDeletedFromCache method [Offline Files], ItemDeletedFromCache method [Offline Files],IOfflineFilesEvents interface, cscobj/IOfflineFilesEvents::ItemDeletedFromCache, of.iofflinefilesevents_itemdeletedfromcache
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: OFFLINEFILES_SYNC_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CscSvc.dll
-	CscObj.dll
api_name:
-	IOfflineFilesEvents.ItemDeletedFromCache
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IOfflineFilesEvents::ItemDeletedFromCache


## -description


Reports that an item has been removed from the Offline Files cache.


## -parameters




### -param pszPath [in]

The item's UNC path string.


### -param ItemType [in]

An <a href="https://msdn.microsoft.com/cf8bb079-d691-4b37-b408-d1af1746ed37">OFFLINEFILES_ITEM_TYPE</a> enumeration value that indicates the type of the item.


## -returns



The return value is ignored.




## -see-also




<a href="https://msdn.microsoft.com/c0bd0033-e5e1-4d21-8d98-eb937acdd6cf">IOfflineFilesEvents</a>
 

 

