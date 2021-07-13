---
UID: NF:objidl.IPersistStorage.HandsOffStorage
title: IPersistStorage::HandsOffStorage (objidl.h)
description: Instructs the object to release all storage objects that have been passed to it by its container and to enter HandsOff mode.
helpviewer_keywords: ["HandsOffStorage","HandsOffStorage method [COM]","HandsOffStorage method [COM]","IPersistStorage interface","IPersistStorage interface [COM]","HandsOffStorage method","IPersistStorage.HandsOffStorage","IPersistStorage::HandsOffStorage","_com_ipersiststorage_handsoffstorage","com.ipersiststorage_handsoffstorage","objidl/IPersistStorage::HandsOffStorage"]
old-location: com\ipersiststorage_handsoffstorage.htm
tech.root: com
ms.assetid: 1e5ef26f-d8e7-4fa6-bfc4-19dace35314d
ms.date: 12/05/2018
ms.keywords: HandsOffStorage, HandsOffStorage method [COM], HandsOffStorage method [COM],IPersistStorage interface, IPersistStorage interface [COM],HandsOffStorage method, IPersistStorage.HandsOffStorage, IPersistStorage::HandsOffStorage, _com_ipersiststorage_handsoffstorage, com.ipersiststorage_handsoffstorage, objidl/IPersistStorage::HandsOffStorage
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
 - IPersistStorage::HandsOffStorage
 - objidl/IPersistStorage::HandsOffStorage
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
 - IPersistStorage.HandsOffStorage
---

# IPersistStorage::HandsOffStorage


## -description

Instructs the object to release all storage objects that have been passed to it by its container and to enter HandsOff mode.



## -returns

This method returns S_OK to indicate that the object has entered HandsOff mode successfully.

## -remarks

This method causes an object to release any storage objects that it is holding and to enter the HandsOff mode until a subsequent <a href="/windows/desktop/api/objidl/nf-objidl-ipersiststorage-savecompleted">IPersistStorage::SaveCompleted</a> call. In HandsOff mode, the object cannot do anything and the only operation that works is a close operation.

A container application typically calls this method during a full save or low-memory full save operation to force the object to release all pointers to its current storage. In these scenarios, the <b>HandsOffStorage</b> call comes after a call to either <a href="/windows/desktop/api/ole2/nf-ole2-olesave">OleSave</a> or <a href="/windows/desktop/api/objidl/nf-objidl-ipersiststorage-save">IPersistStorage::Save</a>, putting the object in HandsOffAfterSave mode. Calling this method is necessary so the container application can delete the current file as part of a full save, or so it can call the <a href="/windows/desktop/api/objidl/nf-objidl-irootstorage-switchtofile">IRootStorage::SwitchToFile</a> method as part of a low-memory save.

A container application also calls this method when an object is in Normal mode to put the object in HandsOffFromNormal mode.

While the component object is in either HandsOffAfterSave or HandsOffFromNormal mode, most operations on the object will fail. Thus, the container should restore the object to Normal mode as soon as possible. The container application does this by calling the <a href="/windows/desktop/api/objidl/nf-objidl-ipersiststorage-savecompleted">IPersistStorage::SaveCompleted</a> method, which passes a storage pointer back to the component object for the new storage object.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
This method must release all pointers to the current storage object, including pointers to any nested streams and storages. If the object contains nested objects, the container application must recursively call this method for any nested objects that are loaded or running.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-ipersiststorage">IPersistStorage</a>



<a href="/windows/desktop/api/ole2/nf-ole2-olesave">OleSave</a>
