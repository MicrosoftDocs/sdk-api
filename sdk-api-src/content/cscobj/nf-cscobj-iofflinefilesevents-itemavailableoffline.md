---
UID: NF:cscobj.IOfflineFilesEvents.ItemAvailableOffline
title: IOfflineFilesEvents::ItemAvailableOffline
author: windows-sdk-content
description: Reports that an item in the Offline Files cache is now available for offline use should the remote copy become unavailable.
old-location: of\iofflinefilesevents_itemavailableoffline.htm
tech.root: offlinefiles
ms.assetid: 6c629ede-00ee-4f5e-9f75-022e3c5b3957
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IOfflineFilesEvents interface [Offline Files],ItemAvailableOffline method, IOfflineFilesEvents.ItemAvailableOffline, IOfflineFilesEvents::ItemAvailableOffline, ItemAvailableOffline, ItemAvailableOffline method [Offline Files], ItemAvailableOffline method [Offline Files],IOfflineFilesEvents interface, cscobj/IOfflineFilesEvents::ItemAvailableOffline, of.iofflinefilesevents_itemavailableoffline
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
 - IOfflineFilesEvents.ItemAvailableOffline
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOfflineFilesEvents::ItemAvailableOffline


## -description


Reports that an item in the Offline Files cache is now available for offline use should the remote copy become unavailable.


## -parameters




### -param pszPath [in]

The item's UNC path string.


### -param ItemType [in]

An <a href="https://msdn.microsoft.com/cf8bb079-d691-4b37-b408-d1af1746ed37">OFFLINEFILES_ITEM_TYPE</a> enumeration value that indicates the type of the item.


## -returns



The return value is ignored.




## -see-also




<a href="https://msdn.microsoft.com/c0bd0033-e5e1-4d21-8d98-eb937acdd6cf">IOfflineFilesEvents</a>
 

 

