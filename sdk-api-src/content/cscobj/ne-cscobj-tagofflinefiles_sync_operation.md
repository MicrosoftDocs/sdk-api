---
UID: NE:cscobj.tagOFFLINEFILES_SYNC_OPERATION
title: tagOFFLINEFILES_SYNC_OPERATION
author: windows-driver-content
description: Indicates the type of sync operation that was being performed when a sync error was encountered.
old-location: of\offlinefiles_sync_operation.htm
old-project: OfflineFiles
ms.assetid: d32db35c-4789-49e6-8c15-15d44eac95cf
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: OFFLINEFILES_SYNC_OPERATION, OFFLINEFILES_SYNC_OPERATION enumeration [Offline Files], OFFLINEFILES_SYNC_OPERATION_CREATE_COPY_ON_CLIENT, OFFLINEFILES_SYNC_OPERATION_CREATE_COPY_ON_SERVER, OFFLINEFILES_SYNC_OPERATION_DELETE_CLIENT_COPY, OFFLINEFILES_SYNC_OPERATION_DELETE_SERVER_COPY, OFFLINEFILES_SYNC_OPERATION_PIN, OFFLINEFILES_SYNC_OPERATION_PREPARE, OFFLINEFILES_SYNC_OPERATION_SYNC_TO_CLIENT, OFFLINEFILES_SYNC_OPERATION_SYNC_TO_SERVER, cscobj/OFFLINEFILES_SYNC_OPERATION, cscobj/OFFLINEFILES_SYNC_OPERATION_CREATE_COPY_ON_CLIENT, cscobj/OFFLINEFILES_SYNC_OPERATION_CREATE_COPY_ON_SERVER, cscobj/OFFLINEFILES_SYNC_OPERATION_DELETE_CLIENT_COPY, cscobj/OFFLINEFILES_SYNC_OPERATION_DELETE_SERVER_COPY, cscobj/OFFLINEFILES_SYNC_OPERATION_PIN, cscobj/OFFLINEFILES_SYNC_OPERATION_PREPARE, cscobj/OFFLINEFILES_SYNC_OPERATION_SYNC_TO_CLIENT, cscobj/OFFLINEFILES_SYNC_OPERATION_SYNC_TO_SERVER, of.offlinefiles_sync_operation, tagOFFLINEFILES_SYNC_OPERATION
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: OFFLINEFILES_SYNC_OPERATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	CscObj.h
api_name:
-	OFFLINEFILES_SYNC_OPERATION
product: Windows
targetos: Windows
req.lib: CscApi.lib
req.dll: CscApi.dll
req.irql: 
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
 

 

