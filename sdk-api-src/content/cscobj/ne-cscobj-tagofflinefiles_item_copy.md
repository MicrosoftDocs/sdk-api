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

# tagOFFLINEFILES_ITEM_COPY enumeration


## -description


Specifies whether the local, remote, or original copy of an item is being queried.


## -enum-fields




### -field OFFLINEFILES_ITEM_COPY_LOCAL

Retrieve the attributes, time values, or size  of the local copy of the item.  If the item is currently offline, this may be different than the attributes associated with the original copy.


### -field OFFLINEFILES_ITEM_COPY_REMOTE

This enumeration value is reserved for future use.


### -field OFFLINEFILES_ITEM_COPY_ORIGINAL

Retrieve the attributes, time values, or size of the original copy of the item.  The original copy represents the state of the item following the last successful sync of that item, which is the most recent time when the server copy and local copy were identical.


## -see-also




<a href="https://msdn.microsoft.com/5bf8a834-cd5e-46b9-9b7d-b5cc6fb9fe10">IOfflineFilesFileSysInfo::GetAttributes</a>



<a href="https://msdn.microsoft.com/a24b7126-ee9a-40f8-9fcd-8696e756a6b9">IOfflineFilesFileSysInfo::GetFileSize</a>



<a href="https://msdn.microsoft.com/120b3f7c-6a92-4a03-8676-1ad4e4dc96b3">IOfflineFilesFileSysInfo::GetTimes</a>
 

 

