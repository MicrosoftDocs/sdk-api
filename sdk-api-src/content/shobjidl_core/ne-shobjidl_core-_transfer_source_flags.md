---
UID: NE:shobjidl_core._TRANSFER_SOURCE_FLAGS
title: _TRANSFER_SOURCE_FLAGS (shobjidl_core.h)
description: Used by methods of the ITransferSource and ITransferDestination interfaces to control their file operations.helpviewer_keywords: ["TRANSFER_SOURCE_FLAGS","TRANSFER_SOURCE_FLAGS enumeration [Windows Shell]","TSF_ALLOW_DECRYPTION","TSF_COPY_CREATION_TIME","TSF_COPY_HARD_LINK","TSF_COPY_LOCALIZED_NAME","TSF_COPY_WRITE_TIME","TSF_DELETE_RECYCLE_IF_POSSIBLE","TSF_FAIL_EXIST","TSF_MOVE_AS_COPY_DELETE","TSF_NORMAL","TSF_NO_SECURITY","TSF_OVERWRITE_EXIST","TSF_RENAME_EXIST","TSF_SUSPEND_SHELLEVENTS","TSF_USE_FULL_ACCESS","_TRANSFER_SOURCE_FLAGS","_shell_TSF_constants","shell.TSF_constants","shobjidl_core/TRANSFER_SOURCE_FLAGS","shobjidl_core/TSF_ALLOW_DECRYPTION","shobjidl_core/TSF_COPY_CREATION_TIME","shobjidl_core/TSF_COPY_HARD_LINK","shobjidl_core/TSF_COPY_LOCALIZED_NAME","shobjidl_core/TSF_COPY_WRITE_TIME","shobjidl_core/TSF_DELETE_RECYCLE_IF_POSSIBLE","shobjidl_core/TSF_FAIL_EXIST","shobjidl_core/TSF_MOVE_AS_COPY_DELETE","shobjidl_core/TSF_NORMAL","shobjidl_core/TSF_NO_SECURITY","shobjidl_core/TSF_OVERWRITE_EXIST","shobjidl_core/TSF_RENAME_EXIST","shobjidl_core/TSF_SUSPEND_SHELLEVENTS","shobjidl_core/TSF_USE_FULL_ACCESS"]
old-location: shell\TSF_constants.htm
tech.root: shell
ms.assetid: 8a3da00a-1d96-444d-acbe-9327620b8d24
ms.date: 12/05/2018
ms.keywords: TRANSFER_SOURCE_FLAGS, TRANSFER_SOURCE_FLAGS enumeration [Windows Shell], TSF_ALLOW_DECRYPTION, TSF_COPY_CREATION_TIME, TSF_COPY_HARD_LINK, TSF_COPY_LOCALIZED_NAME, TSF_COPY_WRITE_TIME, TSF_DELETE_RECYCLE_IF_POSSIBLE, TSF_FAIL_EXIST, TSF_MOVE_AS_COPY_DELETE, TSF_NORMAL, TSF_NO_SECURITY, TSF_OVERWRITE_EXIST, TSF_RENAME_EXIST, TSF_SUSPEND_SHELLEVENTS, TSF_USE_FULL_ACCESS, _TRANSFER_SOURCE_FLAGS, _shell_TSF_constants, shell.TSF_constants, shobjidl_core/TRANSFER_SOURCE_FLAGS, shobjidl_core/TSF_ALLOW_DECRYPTION, shobjidl_core/TSF_COPY_CREATION_TIME, shobjidl_core/TSF_COPY_HARD_LINK, shobjidl_core/TSF_COPY_LOCALIZED_NAME, shobjidl_core/TSF_COPY_WRITE_TIME, shobjidl_core/TSF_DELETE_RECYCLE_IF_POSSIBLE, shobjidl_core/TSF_FAIL_EXIST, shobjidl_core/TSF_MOVE_AS_COPY_DELETE, shobjidl_core/TSF_NORMAL, shobjidl_core/TSF_NO_SECURITY, shobjidl_core/TSF_OVERWRITE_EXIST, shobjidl_core/TSF_RENAME_EXIST, shobjidl_core/TSF_SUSPEND_SHELLEVENTS, shobjidl_core/TSF_USE_FULL_ACCESS
f1_keywords:
- shobjidl_core/TRANSFER_SOURCE_FLAGS
dev_langs:
- c++
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- shobjidl_core.h
api_name:
- TRANSFER_SOURCE_FLAGS
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# _TRANSFER_SOURCE_FLAGS enumeration


## -description


Used by methods of the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransfersource">ITransferSource</a> and <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransferdestination">ITransferDestination</a> interfaces to control their file operations.


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




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransferdestination-createitem">ITransferDestination::CreateItem</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransfersource-linkitem">ITransferSource::LinkItem</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransfersource-moveitem">ITransferSource::MoveItem</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransfersource-openitem">ITransferSource::OpenItem</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransfersource-recycleitem">ITransferSource::RecycleItem</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransfersource-removeitem">ITransferSource::RemoveItem</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransfersource-renameitem">ITransferSource::RenameItem</a>
 

 

