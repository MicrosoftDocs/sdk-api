---
UID: NF:cscobj.IOfflineFilesEvents.ItemRenamed
title: IOfflineFilesEvents::ItemRenamed
author: windows-sdk-content
description: Reports that the path for an item in the Offline Files cache has been renamed.
old-location: of\iofflinefilesevents_itemrenamed.htm
tech.root: OfflineFiles
ms.assetid: f1a678dd-9a02-41da-90d4-930c0d366a36
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IOfflineFilesEvents interface [Offline Files],ItemRenamed method, IOfflineFilesEvents.ItemRenamed, IOfflineFilesEvents::ItemRenamed, ItemRenamed, ItemRenamed method [Offline Files], ItemRenamed method [Offline Files],IOfflineFilesEvents interface, cscobj/IOfflineFilesEvents::ItemRenamed, of.iofflinefilesevents_itemrenamed
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
 - IOfflineFilesEvents.ItemRenamed
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOfflineFilesEvents::ItemRenamed


## -description


Reports that the path for an item in the Offline Files cache has been renamed.


## -parameters




### -param pszOldPath [in]

Original UNC path string for the item.


### -param pszNewPath [in]

New UNC path string for the item.


### -param ItemType [in]

An <a href="https://msdn.microsoft.com/en-us/library/Bb530648(v=VS.85).aspx">OFFLINEFILES_ITEM_TYPE</a> enumeration value that indicates the type of the item.


## -returns



The return value is ignored.




## -remarks



This event is sent whenever a server, share, directory or file is renamed in the cache.  Note that this is a rename resulting from a file system rename operation, not from <a href="https://msdn.microsoft.com/en-us/library/Bb530500(v=VS.85).aspx">IOfflineFilesCache::RenameItem</a> or <a href="https://msdn.microsoft.com/en-us/library/Hh769077(v=VS.85).aspx">IOfflineFilesCache2::RenameItemEx</a>.  (The rename in response to <b>RenameItem</b> or <b>RenameItemEx</b> is performed on system startup by the Offline Files driver before the Offline Files service is operational.)




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb530520(v=VS.85).aspx">IOfflineFilesEvents</a>
 

 

