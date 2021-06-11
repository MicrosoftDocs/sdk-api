---
UID: NF:objidl.IRootStorage.SwitchToFile
title: IRootStorage::SwitchToFile (objidl.h)
description: The SwitchToFile method copies the current file associated with the storage object to a new file.
helpviewer_keywords: ["IRootStorage interface [Structured Storage]","SwitchToFile method","IRootStorage.SwitchToFile","IRootStorage::SwitchToFile","SwitchToFile","SwitchToFile method [Structured Storage]","SwitchToFile method [Structured Storage]","IRootStorage interface","_stg_irootstorage_switchtofile","objidl/IRootStorage::SwitchToFile","stg.irootstorage_switchtofile"]
old-location: stg\irootstorage_switchtofile.htm
tech.root: Stg
ms.assetid: d482b51a-7159-4aab-ac5e-3f1878d426b2
ms.date: 12/05/2018
ms.keywords: IRootStorage interface [Structured Storage],SwitchToFile method, IRootStorage.SwitchToFile, IRootStorage::SwitchToFile, SwitchToFile, SwitchToFile method [Structured Storage], SwitchToFile method [Structured Storage],IRootStorage interface, _stg_irootstorage_switchtofile, objidl/IRootStorage::SwitchToFile, stg.irootstorage_switchtofile
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
 - IRootStorage::SwitchToFile
 - objidl/IRootStorage::SwitchToFile
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
 - IRootStorage.SwitchToFile
---

# IRootStorage::SwitchToFile


## -description

The 
<b>SwitchToFile</b> method copies the current file associated with the storage object to a new file. The new file is then used for the storage object and any uncommitted changes.

## -parameters

### -param pszFile

A pointer to a null terminated string that specifies the file name for the new file. It cannot be the name of an existing file. If <b>NULL</b>, this method creates a temporary file with a unique name, and you can call 
<a href="/windows/desktop/api/objidl/nf-objidl-istorage-stat">IStorage::Stat</a> to retrieve the name of the temporary file.

## -returns

This method can return one of these values.

| Return code | Description |
|----------------|---------------|
|S_OK | The file was successfully copied.|
|STG_E_MEDIUMFULL | The file was not copied because of insufficient space on the storage device.|
|STG_E_ACCESSDENIED | The file was not copied because the caller does not have permission to access storage device.|
|STG_E_INVALIDPOINTER | The file was not copied because the *pszFile* pointer is not valid.|
|STG_E_FILEALREADYEXISTS | The file was not copied because the new filename (*pszFile*) points to an existing file.|

## -remarks

The <b>IRootStorage::SwitchToFile</b> method copies the file associated with the storage object. A COM container calls 
<b>SwitchToFile</b> to perform a full save on a file in a low-memory situation. Typically, this is done only after a normal, full save operation (that is, save to temporary file, delete original file, rename temporary file) has failed with an E_OUTOFMEMORY error.

It is erroneous to call the 
<b>SwitchToFile</b> method if the storage object or anything contained within it has been marshaled to another process. Before calling 
<b>SwitchToFile</b>, the container must call the 
<a href="/windows/desktop/api/objidl/nf-objidl-ipersiststorage-handsoffstorage">IPersistStorage::HandsOffStorage</a> method for any element within the storage object that is loaded or running. The <b>HandsOffStorage</b> method forces the element to release its storage pointers and enter the hands-off storage mode. The container must also release all pointers to streams or storages that are contained in this root storage. After the full save operation is completed, the container returns the contained elements to normal storage mode.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
If you are implementing your own storage objects, the 
<a href="/windows/desktop/api/objidl/nn-objidl-irootstorage">IRootStorage</a> methods (including <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a>, <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a>, and <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a>) must not consume additional memory or file handles.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-ipersiststorage-handsoffstorage">IPersistStorage::HandsOffStorage</a>



<a href="/windows/desktop/api/objidl/nf-objidl-ipersiststorage-savecompleted">IPersistStorage::SaveCompleted</a>



<a href="/windows/desktop/api/objidl/nf-objidl-istorage-commit">IStorage::Commit</a>



<a href="/windows/desktop/api/objidl/nf-objidl-istorage-stat">IStorage::Stat</a>