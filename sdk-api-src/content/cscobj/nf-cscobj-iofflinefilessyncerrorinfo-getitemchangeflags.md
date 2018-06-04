---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IOfflineFilesSyncErrorInfo::GetItemChangeFlags


## -description


Retrieves a value containing a set of flags that describe what changes were encountered during the sync operation associated with the sync error.


## -parameters




### -param pdwItemChangeFlags [out]

Receives a set of flags describing what changes were encountered during the sync operation.  This parameter can be one or more of the following flag values:



#### OFFLINEFILES_SYNC_ITEM_CHANGE_NONE (0x00000000)

No changes were detected.



#### OFFLINEFILES_SYNC_ITEM_CHANGE_CHANGETIME (0x00000001)

The item's last-change time was found to be different between client and server.



#### OFFLINEFILES_SYNC_ITEM_CHANGE_WRITETIME (0x00000002)

The item's write time was found to be different between client and server.



#### OFFLINEFILES_SYNC_ITEM_CHANGE_FILESIZE (0x00000004)

The item's size was found to be different between client and server.



#### OFFLINEFILES_SYNC_ITEM_CHANGE_ATTRIBUTES (0x00000008)

One or more of the item's attributes were found to be different between client and server.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -see-also




<a href="https://msdn.microsoft.com/df1dd351-eb18-46e6-b778-852f551adfd1">IOfflineFilesSyncErrorInfo</a>
 

 

