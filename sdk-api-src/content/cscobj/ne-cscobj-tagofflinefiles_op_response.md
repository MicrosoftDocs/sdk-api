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

# tagOFFLINEFILES_OP_RESPONSE enumeration


## -description


Specifies whether to continue, retry, or stop processing items.


## -enum-fields




### -field OFFLINEFILES_OP_CONTINUE

Continue processing items.


### -field OFFLINEFILES_OP_RETRY

Repeat processing of this item.


### -field OFFLINEFILES_OP_ABORT

Stop processing now.


## -see-also




<a href="https://msdn.microsoft.com/0e3496ee-e987-4c37-93ff-bc8409acabde">IOfflineFilesSimpleProgress::ItemBegin</a>



<a href="https://msdn.microsoft.com/60ed3b12-b56e-4a58-8e37-a4a745ddb783">IOfflineFilesSimpleProgress::ItemResult</a>



<a href="https://msdn.microsoft.com/c1cdbc30-bcc9-4023-a3a2-070fb9958609">IOfflineFilesSyncProgress::SyncItemBegin</a>



<a href="https://msdn.microsoft.com/2a93d52e-6b91-4d91-9372-5f0718621841">IOfflineFilesSyncProgress::SyncItemResult</a>
 

 

