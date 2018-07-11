---
UID: NF:cscobj.IOfflineFilesEvents.ItemDisconnected
title: IOfflineFilesEvents::ItemDisconnected
author: windows-sdk-content
description: Reports that an item in the Offline Files cache has transitioned from online to offline.
old-location: of\iofflinefilesevents_itemdisconnected.htm
old-project: offlinefiles
ms.assetid: b0f9d873-cda5-4805-bb5e-d23d47b53f1d
ms.author: windowssdkdev
ms.date: 05/14/2018
ms.keywords: IOfflineFilesEvents interface [Offline Files],ItemDisconnected method, IOfflineFilesEvents.ItemDisconnected, IOfflineFilesEvents::ItemDisconnected, ItemDisconnected, ItemDisconnected method [Offline Files], ItemDisconnected method [Offline Files],IOfflineFilesEvents interface, cscobj/IOfflineFilesEvents::ItemDisconnected, of.iofflinefilesevents_itemdisconnected
ms.prod: windows
ms.technology: windows-sdk
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
 - IOfflineFilesEvents.ItemDisconnected
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IOfflineFilesEvents::ItemDisconnected


## -description


Reports that an item in the Offline Files cache has transitioned from online to offline.


## -parameters




### -param pszPath [in]

The item's UNC path string.


### -param ItemType [in]

An <a href="https://msdn.microsoft.com/cf8bb079-d691-4b37-b408-d1af1746ed37">OFFLINEFILES_ITEM_TYPE</a> enumeration value that indicates the type of the item.


## -returns



The return value is ignored.




## -see-also




<a href="https://msdn.microsoft.com/c0bd0033-e5e1-4d21-8d98-eb937acdd6cf">IOfflineFilesEvents</a>
 

 

