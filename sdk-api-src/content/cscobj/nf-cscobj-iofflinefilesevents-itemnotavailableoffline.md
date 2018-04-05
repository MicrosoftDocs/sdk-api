---
UID: NF:cscobj.IOfflineFilesEvents.ItemNotAvailableOffline
title: IOfflineFilesEvents::ItemNotAvailableOffline method
author: windows-driver-content
description: Reports that an item in the Offline Files cache is no longer available for offline use should the remote copy become unavailable.
old-location: of\iofflinefilesevents_itemnotavailableoffline.htm
old-project: OfflineFiles
ms.assetid: 868938fd-9da2-45fd-a00e-5dda85b4fd61
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IOfflineFilesEvents, IOfflineFilesEvents interface [Offline Files], ItemNotAvailableOffline method, IOfflineFilesEvents::ItemNotAvailableOffline, ItemNotAvailableOffline method [Offline Files], ItemNotAvailableOffline method [Offline Files], IOfflineFilesEvents interface, ItemNotAvailableOffline,IOfflineFilesEvents.ItemNotAvailableOffline, cscobj/IOfflineFilesEvents::ItemNotAvailableOffline, of.iofflinefilesevents_itemnotavailableoffline
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
-	IOfflineFilesEvents.ItemNotAvailableOffline
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IOfflineFilesEvents::ItemNotAvailableOffline method


## -description


Reports that an item in the Offline Files cache is no longer available for offline use should the remote copy become unavailable.


## -parameters




### -param pszPath [in]

The item's UNC path string.


### -param ItemType [in]

An <a href="https://msdn.microsoft.com/cf8bb079-d691-4b37-b408-d1af1746ed37">OFFLINEFILES_ITEM_TYPE</a> enumeration value that indicates the type of the item.


## -returns



The return value is ignored.




## -remarks



Receipt of this event does not mean the file has been removed from the cache.  The event <a href="https://msdn.microsoft.com/358b358a-65cc-4f37-8beb-be492b83c222">ItemDeletedFromCache</a> is sent when an item has been removed.




## -see-also




<a href="https://msdn.microsoft.com/c0bd0033-e5e1-4d21-8d98-eb937acdd6cf">IOfflineFilesEvents</a>
 

 

