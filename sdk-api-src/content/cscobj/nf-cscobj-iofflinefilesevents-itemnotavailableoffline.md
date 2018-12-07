---
UID: NF:cscobj.IOfflineFilesEvents.ItemNotAvailableOffline
title: IOfflineFilesEvents::ItemNotAvailableOffline
author: windows-sdk-content
description: Reports that an item in the Offline Files cache is no longer available for offline use should the remote copy become unavailable.
old-location: of\iofflinefilesevents_itemnotavailableoffline.htm
tech.root: offlinefiles
ms.assetid: 868938fd-9da2-45fd-a00e-5dda85b4fd61
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IOfflineFilesEvents interface [Offline Files],ItemNotAvailableOffline method, IOfflineFilesEvents.ItemNotAvailableOffline, IOfflineFilesEvents::ItemNotAvailableOffline, ItemNotAvailableOffline, ItemNotAvailableOffline method [Offline Files], ItemNotAvailableOffline method [Offline Files],IOfflineFilesEvents interface, cscobj/IOfflineFilesEvents::ItemNotAvailableOffline, of.iofflinefilesevents_itemnotavailableoffline
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
 - IOfflineFilesEvents.ItemNotAvailableOffline
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOfflineFilesEvents::ItemNotAvailableOffline


## -description


Reports that an item in the Offline Files cache is no longer available for offline use should the remote copy become unavailable.


## -parameters




### -param pszPath [in]

The item's UNC path string.


### -param ItemType [in]

An <a href="https://msdn.microsoft.com/en-us/library/Bb530648(v=VS.85).aspx">OFFLINEFILES_ITEM_TYPE</a> enumeration value that indicates the type of the item.


## -returns



The return value is ignored.




## -remarks



Receipt of this event does not mean the file has been removed from the cache.  The event <a href="https://msdn.microsoft.com/en-us/library/Bb530547(v=VS.85).aspx">ItemDeletedFromCache</a> is sent when an item has been removed.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb530520(v=VS.85).aspx">IOfflineFilesEvents</a>
 

 

