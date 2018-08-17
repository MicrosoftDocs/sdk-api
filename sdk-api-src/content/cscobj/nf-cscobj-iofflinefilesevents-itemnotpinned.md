---
UID: NF:cscobj.IOfflineFilesEvents.ItemNotPinned
title: IOfflineFilesEvents::ItemNotPinned
author: windows-sdk-content
description: Reports that an item in the Offline Files cache is no longer pinned.
old-location: of\iofflinefilesevents_itemnotpinned.htm
old-project: offlinefiles
ms.assetid: cefd7408-9e98-48a4-ad43-0bdef9da1c95
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IOfflineFilesEvents interface [Offline Files],ItemNotPinned method, IOfflineFilesEvents.ItemNotPinned, IOfflineFilesEvents::ItemNotPinned, ItemNotPinned, ItemNotPinned method [Offline Files], ItemNotPinned method [Offline Files],IOfflineFilesEvents interface, cscobj/IOfflineFilesEvents::ItemNotPinned, of.iofflinefilesevents_itemnotpinned
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: cscobj.h
req.include-header: 
req.redist: 
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
 - IOfflineFilesEvents.ItemNotPinned
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IOfflineFilesEvents::ItemNotPinned


## -description


Reports that an item in the Offline Files cache is no longer pinned.  The item may still be available offline but it is now considered automatically cached.


## -parameters




### -param pszPath [in]

The item's UNC path string.


### -param ItemType [in]

An <a href="https://msdn.microsoft.com/en-us/library/Bb530648(v=VS.85).aspx">OFFLINEFILES_ITEM_TYPE</a> enumeration value that indicates the type of the item.


## -returns



The return value is ignored.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb530520(v=VS.85).aspx">IOfflineFilesEvents</a>
 

 

