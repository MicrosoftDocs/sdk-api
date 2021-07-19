---
UID: NF:objidl.IStorage.DestroyElement
title: IStorage::DestroyElement (objidl.h)
description: Removes the specified storage or stream from this storage object.
helpviewer_keywords: ["DestroyElement","DestroyElement method [Structured Storage]","DestroyElement method [Structured Storage]","IStorage interface","IStorage interface [Structured Storage]","DestroyElement method","IStorage.DestroyElement","IStorage::DestroyElement","_stg_istorage_destroyelement","objidl/IStorage::DestroyElement","stg.istorage_destroyelement"]
old-location: stg\istorage_destroyelement.htm
tech.root: Stg
ms.assetid: 70ad7f8c-15ea-42f1-ac18-006bc6ad5e81
ms.date: 12/05/2018
ms.keywords: DestroyElement, DestroyElement method [Structured Storage], DestroyElement method [Structured Storage],IStorage interface, IStorage interface [Structured Storage],DestroyElement method, IStorage.DestroyElement, IStorage::DestroyElement, _stg_istorage_destroyelement, objidl/IStorage::DestroyElement, stg.istorage_destroyelement
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
 - IStorage::DestroyElement
 - objidl/IStorage::DestroyElement
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
 - IStorage.DestroyElement
---

# IStorage::DestroyElement


## -description

The 
<b>DestroyElement</b> method
			 removes the specified storage or stream from this storage object.

## -parameters

### -param pwcsName [in]

A pointer to a wide character null-terminated Unicode string that contains the name of the storage or stream to be removed.

## -returns

This method can return one of these values.

| Return code | Description |
|----------------|---------------|
|S_OK | The element was successfully removed.|
|E_PENDING | Asynchronous Storage only: Part or all of the element data is currently unavailable. |
|STG_E_ACCESSDENIED | The caller does not have permissions to remove the element.|
|STG_E_FILENOTFOUND | The element with the specified name does not exist.|
|STG_E_INSUFFICIENTMEMORY | The element was not removed due to a lack of memory.|
|STG_E_INVALIDNAME | Invalid value for *pwcsName*.|
|STG_E_INVALIDPOINTER | The pointer specified for the element was not valid.|
|STG_E_INVALIDPARAMETER | One of the parameters was not valid.|
|STG_E_REVERTED | The storage object has been invalidated by a revert operation above it in the transaction tree.|
|STG_E_TOOMANYOPENFILES | The element was not removed because there are too many open files.|

## -remarks

The 
<b>DestroyElement</b> method deletes a substorage or stream from the current storage object. After a successful call to 
<b>DestroyElement</b>, any open instance of the destroyed element from the parent storage becomes invalid.

If a storage object is opened in the transacted mode, destruction of an element requires that the call to 
<b>DestroyElement</b> be followed by a call to <a href="/windows/desktop/api/objidl/nf-objidl-istorage-commit">IStorage::Commit</a>.

<div class="alert"><b>Note</b>  The <b>DestroyElement</b> method does not shrink the directory stream.  It only marks the deleted directory entry as invalid.  Invalid entries are reused when creating a new storage or stream.  <p class="note">For content streams, the deleted stream sectors are marked as free. If the free sectors are at the end of the file, the document file should shrink.  To compact a document file, call <b>IStorage::CopyTo</b> on the root storage object and copy to a new storage object.

</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Stg/istorage-compound-file-implementation">IStorage - Compound File Implementation</a>