---
UID: NF:cscobj.IOfflineFilesEvents.ItemAddedToCache
title: IOfflineFilesEvents::ItemAddedToCache (cscobj.h)
description: Reports that an item has been added to the Offline Files cache.helpviewer_keywords: ["IOfflineFilesEvents interface [Offline Files]","ItemAddedToCache method","IOfflineFilesEvents.ItemAddedToCache","IOfflineFilesEvents::ItemAddedToCache","ItemAddedToCache","ItemAddedToCache method [Offline Files]","ItemAddedToCache method [Offline Files]","IOfflineFilesEvents interface","cscobj/IOfflineFilesEvents::ItemAddedToCache","of.iofflinefilesevents_itemaddedtocache"]
old-location: of\iofflinefilesevents_itemaddedtocache.htm
tech.root: offlinefiles
ms.assetid: 7ab04b07-f72a-4a04-a470-4b85c21005c0
ms.date: 12/05/2018
ms.keywords: IOfflineFilesEvents interface [Offline Files],ItemAddedToCache method, IOfflineFilesEvents.ItemAddedToCache, IOfflineFilesEvents::ItemAddedToCache, ItemAddedToCache, ItemAddedToCache method [Offline Files], ItemAddedToCache method [Offline Files],IOfflineFilesEvents interface, cscobj/IOfflineFilesEvents::ItemAddedToCache, of.iofflinefilesevents_itemaddedtocache
f1_keywords:
- cscobj/IOfflineFilesEvents.ItemAddedToCache
dev_langs:
- c++
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
- IOfflineFilesEvents.ItemAddedToCache
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOfflineFilesEvents::ItemAddedToCache


## -description


Reports that an item has been added to the Offline Files cache.


## -parameters




### -param pszPath [in]

The item's UNC path string.


### -param ItemType [in]

An <a href="https://docs.microsoft.com/windows/desktop/api/cscobj/ne-cscobj-offlinefiles_item_type">OFFLINEFILES_ITEM_TYPE</a> enumeration value that indicates the type of the item.


## -returns



The return value is ignored.




## -remarks



Note that addition to the cache does not mean that the item is available for offline use.  It may still be sparsely cached.  When the item is available for offline use, the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesevents-itemavailableoffline">ItemAvailableOffline</a> event will be sent.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesevents">IOfflineFilesEvents</a>
 

 

