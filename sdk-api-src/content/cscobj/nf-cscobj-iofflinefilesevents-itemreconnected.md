---
UID: NF:cscobj.IOfflineFilesEvents.ItemReconnected
title: IOfflineFilesEvents::ItemReconnected
author: windows-sdk-content
description: Reports that an item in the Offline Files cache has transitioned from offline to online.
old-location: of\iofflinefilesevents_itemreconnected.htm
tech.root: OfflineFiles
ms.assetid: beafae9d-3ef8-401f-8ab6-79d2ae3366a4
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IOfflineFilesEvents interface [Offline Files],ItemReconnected method, IOfflineFilesEvents.ItemReconnected, IOfflineFilesEvents::ItemReconnected, ItemReconnected, ItemReconnected method [Offline Files], ItemReconnected method [Offline Files],IOfflineFilesEvents interface, cscobj/IOfflineFilesEvents::ItemReconnected, of.iofflinefilesevents_itemreconnected
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
 - IOfflineFilesEvents.ItemReconnected
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
- IOfflineFilesEvents.ItemReconnected
: 
---

# IOfflineFilesEvents::ItemReconnected


## -description


Reports that an item in the Offline Files cache has transitioned from offline to online.


## -parameters




### -param pszPath [in]

The item's UNC path string.


### -param ItemType [in]

An <a href="https://msdn.microsoft.com/en-us/library/Bb530648(v=VS.85).aspx">OFFLINEFILES_ITEM_TYPE</a> enumeration value that indicates the type of the item.


## -returns



The return value is ignored.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb530520(v=VS.85).aspx">IOfflineFilesEvents</a>
 

 

