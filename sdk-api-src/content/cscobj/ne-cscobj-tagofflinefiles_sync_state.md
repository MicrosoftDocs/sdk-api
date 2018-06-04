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

# tagOFFLINEFILES_SYNC_STATE enumeration


## -description


Describes the sync state of an Offline Files item.


## -enum-fields




### -field OFFLINEFILES_SYNC_STATE_Stable

The client and server copies of the file are in sync.


### -field OFFLINEFILES_SYNC_STATE_FileOnClient_DirOnServer

The file exists on the client. The directory exists on the server.


### -field OFFLINEFILES_SYNC_STATE_FileOnClient_NoServerCopy

The file exists only on the client.


### -field OFFLINEFILES_SYNC_STATE_DirOnClient_FileOnServer

The directory exists on the client. The file exists on the server.


### -field OFFLINEFILES_SYNC_STATE_DirOnClient_FileChangedOnServer

The directory exists on the client. The server copy of the file has changed.


### -field OFFLINEFILES_SYNC_STATE_DirOnClient_NoServerCopy

The directory exists only on the client.


### -field OFFLINEFILES_SYNC_STATE_FileCreatedOnClient_NoServerCopy

The file was created on the client. There is no server copy of the file.


### -field OFFLINEFILES_SYNC_STATE_FileCreatedOnClient_FileChangedOnServer

The file was created on the client. The server copy of the file has changed.


### -field OFFLINEFILES_SYNC_STATE_FileCreatedOnClient_DirChangedOnServer

The file was created on the client. The directory on the server has changed.


### -field OFFLINEFILES_SYNC_STATE_FileCreatedOnClient_FileOnServer

The file was created on the client. The server has a file with the same name.


### -field OFFLINEFILES_SYNC_STATE_FileCreatedOnClient_DirOnServer

The file was created on the client. A directory with the same name exists on the server.


### -field OFFLINEFILES_SYNC_STATE_FileCreatedOnClient_DeletedOnServer

The file was created on the client. The server copy of the file was deleted.


### -field OFFLINEFILES_SYNC_STATE_FileChangedOnClient_ChangedOnServer

The client copy of the file has changed. The server copy of the file has changed. This value represents the classic change/change sync conflict.


### -field OFFLINEFILES_SYNC_STATE_FileChangedOnClient_DirOnServer

The client copy of the file has changed. The directory exists on the server.


### -field OFFLINEFILES_SYNC_STATE_FileChangedOnClient_DirChangedOnServer

The client copy of the file has changed. The directory on the server has changed.


### -field OFFLINEFILES_SYNC_STATE_FileChangedOnClient_DeletedOnServer

The client copy of the file has changed. The server copy of the file has been deleted.


### -field OFFLINEFILES_SYNC_STATE_FileSparseOnClient_ChangedOnServer

The file is sparsely cached on the client. The server copy of the file has changed.


### -field OFFLINEFILES_SYNC_STATE_FileSparseOnClient_DeletedOnServer

The file is sparsely cached on the client. The server copy of the file has been deleted.


### -field OFFLINEFILES_SYNC_STATE_FileSparseOnClient_DirOnServer

The file is sparsely cached on the client. The directory exists on the server.


### -field OFFLINEFILES_SYNC_STATE_FileSparseOnClient_DirChangedOnServer

The file is sparsely cached on the client. The directory on the server has changed.


### -field OFFLINEFILES_SYNC_STATE_DirCreatedOnClient_NoServerCopy

The directory has been created on the client. There is no server copy of the directory.


### -field OFFLINEFILES_SYNC_STATE_DirCreatedOnClient_DirOnServer

The directory has been created on the client. A directory with the same name exists on the server.


### -field OFFLINEFILES_SYNC_STATE_DirCreatedOnClient_FileOnServer

The directory has been created on the client. A file with the same name exists on the server.


### -field OFFLINEFILES_SYNC_STATE_DirCreatedOnClient_FileChangedOnServer

The directory has been created on the client. The server copy of the file has changed.


### -field OFFLINEFILES_SYNC_STATE_DirCreatedOnClient_DirChangedOnServer

The directory has been created on the client. The directory on the server has changed.


### -field OFFLINEFILES_SYNC_STATE_DirCreatedOnClient_DeletedOnServer

The directory has been created on the client. The directory on the server has been deleted.


### -field OFFLINEFILES_SYNC_STATE_DirChangedOnClient_FileOnServer

The client directory has changed. The server has a copy of the file.


### -field OFFLINEFILES_SYNC_STATE_DirChangedOnClient_FileChangedOnServer

The client directory has changed. The server copy of the file has been changed.


### -field OFFLINEFILES_SYNC_STATE_DirChangedOnClient_ChangedOnServer

The client directory has changed. The server directory has also changed.


### -field OFFLINEFILES_SYNC_STATE_DirChangedOnClient_DeletedOnServer

The client directory has changed. The directory on the server has been deleted.


### -field OFFLINEFILES_SYNC_STATE_NoClientCopy_FileOnServer

The file exists only on the server.


### -field OFFLINEFILES_SYNC_STATE_NoClientCopy_DirOnServer

The directory exists only on the server.


### -field OFFLINEFILES_SYNC_STATE_NoClientCopy_FileChangedOnServer

The file exists only on the server, and the server copy of the file has changed.


### -field OFFLINEFILES_SYNC_STATE_NoClientCopy_DirChangedOnServer

The directory exists only on the server, and the server directory has changed.


### -field OFFLINEFILES_SYNC_STATE_DeletedOnClient_FileOnServer

The file exists only on the server, because the client copy of the file has been deleted.


### -field OFFLINEFILES_SYNC_STATE_DeletedOnClient_DirOnServer

The directory exists only on the server, because the client directory has been deleted.


### -field OFFLINEFILES_SYNC_STATE_DeletedOnClient_FileChangedOnServer

The client copy of the file has been deleted, and the server copy of the file has changed. This value represents the classic delete/change conflict.


### -field OFFLINEFILES_SYNC_STATE_DeletedOnClient_DirChangedOnServer

The client copy of the directory has been deleted, and the server copy of the directory has changed.


### -field OFFLINEFILES_SYNC_STATE_FileSparseOnClient

The file is sparsely cached on the client.


### -field OFFLINEFILES_SYNC_STATE_FileChangedOnClient

The file has been changed on the client.


### -field OFFLINEFILES_SYNC_STATE_FileRenamedOnClient

This value is reserved for future use.


### -field OFFLINEFILES_SYNC_STATE_DirSparseOnClient

The directory is sparsely cached on the client.


### -field OFFLINEFILES_SYNC_STATE_DirChangedOnClient

The directory has been changed on the client.


### -field OFFLINEFILES_SYNC_STATE_DirRenamedOnClient

This value is reserved for future use.


### -field OFFLINEFILES_SYNC_STATE_FileChangedOnServer

The server copy of the file has been changed.


### -field OFFLINEFILES_SYNC_STATE_FileRenamedOnServer

This value is reserved for future use.


### -field OFFLINEFILES_SYNC_STATE_FileDeletedOnServer

The server copy of the file has been deleted.


### -field OFFLINEFILES_SYNC_STATE_DirChangedOnServer

The server directory has been changed.


### -field OFFLINEFILES_SYNC_STATE_DirRenamedOnServer

This value is reserved for future use.


### -field OFFLINEFILES_SYNC_STATE_DirDeletedOnServer

The server directory has been deleted.


### -field OFFLINEFILES_SYNC_STATE_FileReplacedAndDeletedOnClient_FileOnServer

The file has been replaced and deleted on the client. The server has a copy of the file.


### -field OFFLINEFILES_SYNC_STATE_FileReplacedAndDeletedOnClient_FileChangedOnServer

The file has been replaced and deleted on the client. The server copy of the file has changed.


### -field OFFLINEFILES_SYNC_STATE_FileReplacedAndDeletedOnClient_DirOnServer

The file has been replaced and deleted on the client. The directory exists on the server.


### -field OFFLINEFILES_SYNC_STATE_FileReplacedAndDeletedOnClient_DirChangedOnServer

The file has been replaced and deleted on the client. The directory has changed on the server.


### -field OFFLINEFILES_SYNC_STATE_NUMSTATES




## -see-also




<a href="https://msdn.microsoft.com/eb6fbdcf-1833-4ada-880e-f2dbfce64d99">IOfflineFilesSyncConflictHandler::ResolveConflict</a>



<a href="https://msdn.microsoft.com/2082b476-cb98-4845-885a-56731f8a4762">OFFLINEFILES_SYNC_CONFLICT_RESOLVE</a>
 

 

