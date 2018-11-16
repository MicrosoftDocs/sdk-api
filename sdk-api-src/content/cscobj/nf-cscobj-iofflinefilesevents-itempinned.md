---
UID: NF:cscobj.IOfflineFilesEvents.ItemPinned
title: IOfflineFilesEvents::ItemPinned
author: windows-sdk-content
description: Reports that an item in the Offline Files cache is now pinned and guaranteed to be available offline should the remote copy become unavailable.
old-location: of\iofflinefilesevents_itempinned.htm
tech.root: OfflineFiles
ms.assetid: cf298e4e-97c8-4f6f-b6f5-0bd0d9435599
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IOfflineFilesEvents interface [Offline Files],ItemPinned method, IOfflineFilesEvents.ItemPinned, IOfflineFilesEvents::ItemPinned, ItemPinned, ItemPinned method [Offline Files], ItemPinned method [Offline Files],IOfflineFilesEvents interface, cscobj/IOfflineFilesEvents::ItemPinned, of.iofflinefilesevents_itempinned
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
 - IOfflineFilesEvents.ItemPinned
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- cscobj.h
: 
- IOfflineFilesEvents.ItemPinned
: 
---

# IOfflineFilesEvents::ItemPinned


## -description


Reports that an item in the Offline Files cache is now pinned and guaranteed to be available offline should the remote copy become unavailable.


## -parameters




### -param pszPath [in]

The item's UNC path string.


### -param ItemType [in]

An <a href="https://msdn.microsoft.com/cf8bb079-d691-4b37-b408-d1af1746ed37">OFFLINEFILES_ITEM_TYPE</a> enumeration value that indicates the type of the item.


## -returns



The return value is ignored.




## -see-also




<a href="https://msdn.microsoft.com/c0bd0033-e5e1-4d21-8d98-eb937acdd6cf">IOfflineFilesEvents</a>
 

 

