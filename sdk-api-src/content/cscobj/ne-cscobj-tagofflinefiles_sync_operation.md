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

# tagOFFLINEFILES_SYNC_OPERATION enumeration


## -description


Indicates the type of sync operation that was being performed when a sync error was encountered.


## -enum-fields




### -field OFFLINEFILES_SYNC_OPERATION_CREATE_COPY_ON_SERVER

Operation was creating a new file or directory copy on the server.


### -field OFFLINEFILES_SYNC_OPERATION_CREATE_COPY_ON_CLIENT

Operation was creating a new file or directory copy on the client.


### -field OFFLINEFILES_SYNC_OPERATION_SYNC_TO_SERVER

Operation was synchronizing a file or directory from the client to the server.


### -field OFFLINEFILES_SYNC_OPERATION_SYNC_TO_CLIENT

Operation was synchronizing a file or directory from the server to the client.


### -field OFFLINEFILES_SYNC_OPERATION_DELETE_SERVER_COPY

Operation was deleting a copy from the server.


### -field OFFLINEFILES_SYNC_OPERATION_DELETE_CLIENT_COPY

Operation was deleting a copy from the local cache on the client.


### -field OFFLINEFILES_SYNC_OPERATION_PIN

Operation was pinning a file or directory into the local cache.


### -field OFFLINEFILES_SYNC_OPERATION_PREPARE

Operation was preparing for the synchronization.  Preparation involves obtaining directory listings from the client and server, comparing the two, and building a list of items to be synchronized.


## -see-also




<a href="https://msdn.microsoft.com/21973fb8-26f9-40a0-bb9a-d9c5ff6924e7">IOfflineFilesSyncErrorInfo::GetSyncOperation</a>
 

 

