---
UID: NF:objidl.IStorage.CreateStorage
title: IStorage::CreateStorage (objidl.h)
description: Creates and opens a new storage object nested within this storage object with the specified name in the specified access mode.
helpviewer_keywords: ["CreateStorage","CreateStorage method [Structured Storage]","CreateStorage method [Structured Storage]","IStorage interface","IStorage interface [Structured Storage]","CreateStorage method","IStorage.CreateStorage","IStorage::CreateStorage","_stg_istorage_createstorage","objidl/IStorage::CreateStorage","stg.istorage_createstorage"]
old-location: stg\istorage_createstorage.htm
tech.root: Stg
ms.assetid: 8c74cacf-8d3c-4d57-b1e9-dc5e4f281717
ms.date: 12/05/2018
ms.keywords: CreateStorage, CreateStorage method [Structured Storage], CreateStorage method [Structured Storage],IStorage interface, IStorage interface [Structured Storage],CreateStorage method, IStorage.CreateStorage, IStorage::CreateStorage, _stg_istorage_createstorage, objidl/IStorage::CreateStorage, stg.istorage_createstorage
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
 - IStorage::CreateStorage
 - objidl/IStorage::CreateStorage
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
 - IStorage.CreateStorage
---

# IStorage::CreateStorage


## -description

The <b>CreateStorage</b> method
			 creates and opens a new storage object nested within this storage object with the specified name in the specified access mode.

## -parameters

### -param pwcsName [in]

A pointer to a wide character null-terminated Unicode string that contains the name of the newly created storage object. The name can be used later to reopen the storage object. The name must not exceed 31 characters in length, not including the string terminator. The 000 through 01f characters, serving as the first character of the stream/storage name, are reserved for use by OLE. This is a compound file restriction, not a structured storage restriction.

### -param grfMode [in]

A value that specifies the access mode to use when opening the newly created storage object. For more information and a description of possible values, see <a href="/windows/desktop/Stg/stgm-constants">STGM Constants</a>.

### -param reserved1 [in]

Reserved for future use; must be zero.

### -param reserved2 [in]

Reserved for future use; must be zero.

### -param ppstg [out]

A pointer, when successful, to the location of the 
<a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> pointer to the newly created storage object. This parameter is set to <b>NULL</b> if an error occurs.

## -returns

This method can return one of these values.

| Return code | Description |
|----------------|---------------|
|S_OK | The storage object was created successfully.|
|E_PENDING | Asynchronous Storage only: Part or all of the necessary data is currently unavailable. |
|STG_E_ACCESSDENIED | Not enough permissions to create storage object.|
|STG_E_FILEALREADYEXISTS | The name specified for the storage object already exists in the storage object and the *grfMode* parameter includes the flag STGM_FAILIFTHERE.|
|STG_E_INSUFFICIENTMEMORY | The storage object was not created due to a lack of memory.|
|STG_E_INVALIDFLAG | The value specified for the *grfMode<* parameter is not a valid *STGM* constant value.|he value specified for the grfMode parameter is not a valid
|STG_E_INVALIDFUNCTION | The specified combination of flags in the *grfMode* parameter is not supported.|
|STG_E_INVALIDNAME | Not a valid value for *pwcsName*.|
|STG_E_INVALIDPOINTER | The pointer specified for the storage object was not valid.|
|STG_E_INVALIDPARAMETER | One of the parameters was not valid.|
|STG_E_REVERTED | The storage object has been invalidated by a revert operation above it in the transaction tree.|
|STG_E_TOOMANYOPENFILES | The storage object was not created because there are too many open files.|
|STG_S_CONVERTED | The existing stream with the specified name was replaced with a new storage object containing a single stream called CONTENTS. The new storage object will be added.|

## -remarks

If a storage with the name specified in the <i>pwcsName</i> parameter already exists within the parent storage object, and the <i>grfMode</i> parameter includes the STGM_CREATE flag, the existing storage is replaced by the new one. If the <i>grfMode</i> parameter includes the STGM_CONVERT flag, the existing element is converted to a stream object named CONTENTS and the new storage object is created containing the CONTENTS stream object. The destruction of the old element and the creation of the new storage object are both subject to the transaction mode on the parent storage object. Be aware that you cannot use STGM_CONVERT if you are also using STGM_CREATE.

The COM-provided compound file implementation of the <b>IStorage::CreateStorage</b> method does not support the following behavior:

<ul>
<li>The STGM_PRIORITY flag for nonroot storages.</li>
<li>Opening the same storage object more than once from the same parent storage. The STGM_SHARE_EXCLUSIVE flag must be specified.</li>
<li>The STGM_DELETEONRELEASE flag. If this flag is specified, the function returns STG_E_INVALIDFLAG.</li>
</ul>
If a storage object with the same name already exists and <i>grfMode</i> is set to STGM_FAILIFTHERE, this method fails with the return value STG_E_FILEALREADYEXISTS.

## -see-also

<a href="/windows/desktop/Stg/istorage-compound-file-implementation">IStorage - Compound File Implementation</a>



<a href="/windows/desktop/api/objidl/nf-objidl-istorage-openstorage">IStorage::OpenStorage</a>