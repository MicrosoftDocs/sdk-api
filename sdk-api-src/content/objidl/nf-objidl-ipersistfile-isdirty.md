---
UID: NF:objidl.IPersistFile.IsDirty
title: IPersistFile::IsDirty (objidl.h)
description: Determines whether an object has changed since it was last saved to its current file.
helpviewer_keywords: ["IPersistFile interface [COM]","IsDirty method","IPersistFile.IsDirty","IPersistFile::IsDirty","IsDirty","IsDirty method [COM]","IsDirty method [COM]","IPersistFile interface","_com_ipersistfile_isdirty","com.ipersistfile_isdirty","objidl/IPersistFile::IsDirty"]
old-location: com\ipersistfile_isdirty.htm
tech.root: com
ms.assetid: 4f3df841-d7fe-472e-a13c-124fdf425a35
ms.date: 12/05/2018
ms.keywords: IPersistFile interface [COM],IsDirty method, IPersistFile.IsDirty, IPersistFile::IsDirty, IsDirty, IsDirty method [COM], IsDirty method [COM],IPersistFile interface, _com_ipersistfile_isdirty, com.ipersistfile_isdirty, objidl/IPersistFile::IsDirty
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
 - IPersistFile::IsDirty
 - objidl/IPersistFile::IsDirty
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
 - IPersistFile.IsDirty
---

# IPersistFile::IsDirty


## -description

Determines whether an object has changed since it was last saved to its current file.



## -returns

This method returns S_OK to indicate that the object has changed. Otherwise, it returns S_FALSE.

## -remarks

Use this method to determine whether an object should be saved before closing it. The dirty flag for an object is conditionally cleared in the <a href="/windows/desktop/api/objidl/nf-objidl-ipersistfile-save">IPersistFile::Save</a> method.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
OLE does not call <b>IsDirty</b>. Applications would not call it unless they are also saving an object to a file.

You should treat any error return codes as an indication that the object has changed. Unless this method explicitly returns S_FALSE, assume that the object must be saved.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
An object with no contained objects simply checks its dirty flag to return the appropriate result.

A container with one or more contained objects must maintain an internal dirty flag that is set when any of its contained objects has changed since it was last saved. To do this, the container should maintain an advise sink by implementing the <a href="/windows/desktop/api/objidl/nn-objidl-iadvisesink">IAdviseSink</a> interface. Then, the container can register each link or embedding for data change notifications with a call to <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-dadvise">IDataObject::DAdvise</a>. Then, the container can set its internal dirty flag when it receives an <a href="/windows/desktop/api/objidl/nf-objidl-iadvisesink-ondatachange">IAdviseSink::OnDataChange</a> notification. If the container does not register for data change notifications, the <b>IPersistFile::IsDirty</b> implementation would call <a href="/windows/desktop/api/objidl/nf-objidl-ipersiststorage-isdirty">IPersistStorage::IsDirty</a> for each of its contained objects to determine whether they have changed.

The container can clear its dirty flag whenever it is saved, as long as the file to which the object is saved is the current working file after the save. Therefore, the dirty flag would be cleared after a successful <b>Save</b> or <b>Save As</b> operation, but not after a <b>Save A Copy As . . .</b> operation.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-iadvisesink-ondatachange">IAdviseSink::OnDataChange</a>



<a href="/windows/desktop/api/objidl/nf-objidl-idataobject-dadvise">IDataObject::DAdvise</a>



<a href="/windows/desktop/api/objidl/nn-objidl-ipersistfile">IPersistFile</a>
