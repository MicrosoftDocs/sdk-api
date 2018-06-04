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

# _TRANSFER_SOURCE_FLAGS enumeration


## -description


Used by methods of the <a href="https://msdn.microsoft.com/341966d4-f9cf-457d-97ef-8e6107544283">ITransferSource</a> and <a href="https://msdn.microsoft.com/8d0049e0-e227-40ae-a282-cdc17f227e24">ITransferDestination</a> interfaces to control their file operations.


## -enum-fields




### -field TSF_NORMAL

Fail if the destination already exists, unless TSF_OVERWRITE_EXIST is specified. This is a default behavior.


### -field TSF_FAIL_EXIST

Fail if the destination already exists, unless TSF_OVERWRITE_EXIST is specified. This is a default behavior.


### -field TSF_RENAME_EXIST

Rename with auto-name generation if the destination already exists.


### -field TSF_OVERWRITE_EXIST

Overwrite or merge with the destination.


### -field TSF_ALLOW_DECRYPTION

Allow creation of a decrypted destination.


### -field TSF_NO_SECURITY

No discretionary access control list (DACL), system access control list (SACL), or owner.


### -field TSF_COPY_CREATION_TIME

Copy the creation time as part of the copy. This can be useful for a move operation that is being used as a copy and delete operation (TSF_MOVE_AS_COPY_DELETE).


### -field TSF_COPY_WRITE_TIME

Copy the last write time as part of the copy.


### -field TSF_USE_FULL_ACCESS

Assign write, read, and delete permissions as share mode.


### -field TSF_DELETE_RECYCLE_IF_POSSIBLE

Recycle on file delete, if possible.


### -field TSF_COPY_HARD_LINK

Hard link to the desired source (not required). This avoids a normal copy operation.


### -field TSF_COPY_LOCALIZED_NAME

Copy the localized name.


### -field TSF_MOVE_AS_COPY_DELETE

Move as a copy and delete operation.


### -field TSF_SUSPEND_SHELLEVENTS

Suspend Shell events.


## -see-also




<a href="https://msdn.microsoft.com/56a02dd1-2118-4585-b6e9-8223c086b48a">ITransferDestination::CreateItem</a>



<a href="https://msdn.microsoft.com/e373c790-5366-4bff-a08d-817b0c566b1d">ITransferSource::LinkItem</a>



<a href="https://msdn.microsoft.com/de59291c-12ad-4639-bc10-d8416a979eb7">ITransferSource::MoveItem</a>



<a href="https://msdn.microsoft.com/8f051923-2798-43e9-8e8d-95eec5f618aa">ITransferSource::OpenItem</a>



<a href="https://msdn.microsoft.com/ee99a1ff-1a3e-46a4-82c6-df5f6c26c396">ITransferSource::RecycleItem</a>



<a href="https://msdn.microsoft.com/53084f0d-cf78-437a-ae04-43fd78cb9839">ITransferSource::RemoveItem</a>



<a href="https://msdn.microsoft.com/793eba59-6d21-4c7b-8fdb-bb7658fc410e">ITransferSource::RenameItem</a>
 

 

