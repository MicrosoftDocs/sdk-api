---
UID: NF:objidl.IStorage.RenameElement
title: IStorage::RenameElement (objidl.h)
description: The RenameElement method renames the specified substorage or stream in this storage object.
helpviewer_keywords: ["IStorage interface [Structured Storage]","RenameElement method","IStorage.RenameElement","IStorage::RenameElement","RenameElement","RenameElement method [Structured Storage]","RenameElement method [Structured Storage]","IStorage interface","_stg_istorage_renameelement","objidl/IStorage::RenameElement","stg.istorage_renameelement"]
old-location: stg\istorage_renameelement.htm
tech.root: Stg
ms.assetid: 9d88b2e0-8b68-4607-8f96-5e36e831c283
ms.date: 12/05/2018
ms.keywords: IStorage interface [Structured Storage],RenameElement method, IStorage.RenameElement, IStorage::RenameElement, RenameElement, RenameElement method [Structured Storage], RenameElement method [Structured Storage],IStorage interface, _stg_istorage_renameelement, objidl/IStorage::RenameElement, stg.istorage_renameelement
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IStorage::RenameElement
 - objidl/IStorage::RenameElement
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - IStorage.RenameElement
---

# IStorage::RenameElement


## -description

The <b>RenameElement</b> method renames the specified substorage or stream in this storage object.

## -parameters

### -param pwcsOldName [in]

Pointer to a wide character null-terminated Unicode string that contains the name of the substorage or stream to be changed.

<div class="alert"><b>Note</b>  The <i>pwcsName</i>, created in <a href="/windows/desktop/api/objidl/nf-objidl-istorage-createstorage">CreateStorage</a> or <a href="/windows/desktop/api/objidl/nf-objidl-istorage-createstream">CreateStream</a> must not exceed 31 characters in length, not including the string terminator.</div>
<div> </div>

### -param pwcsNewName [in]

Pointer to a wide character null-terminated unicode string that contains the new name for the specified substorage or stream.

<div class="alert"><b>Note</b>  The <i>pwcsName</i>, created in <a href="/windows/desktop/api/objidl/nf-objidl-istorage-createstorage">CreateStorage</a> or <a href="/windows/desktop/api/objidl/nf-objidl-istorage-createstream">CreateStream</a> must not exceed 31 characters in length, not including the string terminator.</div>
<div> </div>

## -returns

This method can return one of these values.

| Return code | Description |
|----------------|---------------|
|S_OK | The element was successfully renamed.|
|E_PENDING | Asynchronous Storage only: Part or all of the element's data is currently unavailable.|
|STG_E_ACCESSDENIED | The caller does not have enough permissions for renaming the element.|
|STG_E_FILENOTFOUND | The element with the specified old name does not exist.|
|STG_E_FILEALREADYEXISTS | The element specified by the new name already exists.|
|STG_E_INSUFFICIENTMEMORY | The element was not renamed due to a lack of memory.|
|STG_E_INVALIDNAME | Invalid value for one of the names.|
|STG_E_INVALIDPOINTER | The pointer specified for the element was not valid.|
|STG_E_INVALIDPARAMETER | One of the parameters was not valid.|
|STG_E_REVERTED | The storage object has been invalidated by a revert operation above it in the transaction tree.|
|STG_E_TOOMANYOPENFILES | The element was not renamed because there are too many open files.|

## -remarks

<b>IStorage::RenameElement</b> renames the specified substorage or stream in this storage object. An element in a storage object cannot be renamed while it is open. The rename operation is subject to committing the changes if the storage is open in transacted mode.

The <b>IStorage::RenameElement</b> method is not guaranteed to work in low memory with storage objects open in transacted mode. It may work in direct mode.

## -see-also

<a href="/windows/desktop/Stg/istorage-compound-file-implementation">IStorage - Compound File Implementation</a>