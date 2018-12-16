---
UID: NF:cscobj.IOfflineFilesEvents.ItemModified
title: IOfflineFilesEvents::ItemModified
author: windows-sdk-content
description: Reports that an item in the Offline Files cache has been modified.
old-location: of\iofflinefilesevents_itemmodified.htm
tech.root: offlinefiles
ms.assetid: e689b111-d6d1-436e-b468-570e575a5170
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IOfflineFilesEvents interface [Offline Files],ItemModified method, IOfflineFilesEvents.ItemModified, IOfflineFilesEvents::ItemModified, ItemModified, ItemModified method [Offline Files], ItemModified method [Offline Files],IOfflineFilesEvents interface, cscobj/IOfflineFilesEvents::ItemModified, of.iofflinefilesevents_itemmodified
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
 - IOfflineFilesEvents.ItemModified
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOfflineFilesEvents::ItemModified


## -description


Reports that an item in the Offline Files cache has been modified.


## -parameters




### -param pszPath [in]

The item's UNC path string.


### -param ItemType [in]

An <a href="https://msdn.microsoft.com/cf8bb079-d691-4b37-b408-d1af1746ed37">OFFLINEFILES_ITEM_TYPE</a> enumeration value that indicates the type of the item.


### -param bModifiedData [in]

<b>TRUE</b> if the item's data was modified, <b>FALSE</b> otherwise.


### -param bModifiedAttributes [in]

<b>TRUE</b> if one or more of the item's attributes were modified, <b>FALSE</b> otherwise.


## -returns



The return value is ignored.




## -see-also




<a href="https://msdn.microsoft.com/c0bd0033-e5e1-4d21-8d98-eb937acdd6cf">IOfflineFilesEvents</a>
 

 

