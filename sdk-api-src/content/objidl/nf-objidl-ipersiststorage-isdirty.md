---
UID: NF:objidl.IPersistStorage.IsDirty
title: IPersistStorage::IsDirty (objidl.h)
description: Determines whether an object has changed since it was last saved to its current storage.
helpviewer_keywords: ["IPersistStorage interface [COM]","IsDirty method","IPersistStorage.IsDirty","IPersistStorage::IsDirty","IsDirty","IsDirty method [COM]","IsDirty method [COM]","IPersistStorage interface","_com_ipersiststorage_isdirty","com.ipersiststorage_isdirty","objidl/IPersistStorage::IsDirty"]
old-location: com\ipersiststorage_isdirty.htm
tech.root: com
ms.assetid: 604e044f-cede-486e-8b17-c62a1cfd1d28
ms.date: 12/05/2018
ms.keywords: IPersistStorage interface [COM],IsDirty method, IPersistStorage.IsDirty, IPersistStorage::IsDirty, IsDirty, IsDirty method [COM], IsDirty method [COM],IPersistStorage interface, _com_ipersiststorage_isdirty, com.ipersiststorage_isdirty, objidl/IPersistStorage::IsDirty
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPersistStorage::IsDirty
 - objidl/IPersistStorage::IsDirty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IPersistStorage.IsDirty
---

# IPersistStorage::IsDirty


## -description

Determines whether an object has changed since it was last saved to its current storage.



## -returns

This method returns S_OK to indicate that the object has changed. Otherwise, it returns S_FALSE.

## -remarks

Use this method to determine whether an object should be saved before closing it. The dirty flag for an object is conditionally cleared in the <a href="/windows/desktop/api/objidl/nf-objidl-ipersiststorage-save">IPersistStorage::Save</a> method.

For example, you could optimize a <b>File Save</b> operation by calling the <b>IPersistStorage::IsDirty</b> method for each object and then calling the <a href="/windows/desktop/api/objidl/nf-objidl-ipersiststorage-save">IPersistStorage::Save</a> method only for those objects that are dirty.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
You should treat any error return codes as an indication that the object has changed. Unless this method explicitly returns S_FALSE, assume that the object must be saved.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
An object with no contained objects simply checks its dirty flag to return the appropriate result.

A container with one or more contained objects must maintain an internal dirty flag that is set when any of its contained objects has changed since it was last saved.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-ipersiststorage">IPersistStorage</a>
