---
UID: NF:objidl.IPersistStorage.Load
title: IPersistStorage::Load (objidl.h)
description: Loads an object from its existing storage.
helpviewer_keywords: ["IPersistStorage interface [COM]","Load method","IPersistStorage.Load","IPersistStorage::Load","Load","Load method [COM]","Load method [COM]","IPersistStorage interface","_com_ipersiststorage_load","com.ipersiststorage_load","objidl/IPersistStorage::Load"]
old-location: com\ipersiststorage_load.htm
tech.root: com
ms.assetid: 34379b8d-4e00-49cd-9fd1-65f88746c61a
ms.date: 12/05/2018
ms.keywords: IPersistStorage interface [COM],Load method, IPersistStorage.Load, IPersistStorage::Load, Load, Load method [COM], Load method [COM],IPersistStorage interface, _com_ipersiststorage_load, com.ipersiststorage_load, objidl/IPersistStorage::Load
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
 - IPersistStorage::Load
 - objidl/IPersistStorage::Load
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
 - IPersistStorage.Load
---

# IPersistStorage::Load


## -description

Loads an object from its existing storage.

## -parameters

### -param pStg [in]

An <a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> pointer to the existing storage from which the object is to be loaded.

## -returns

This method can return the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_ALREADYINITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The object has already been initialized by a previous call to the <a href="/windows/desktop/api/objidl/nf-objidl-ipersiststorage-load">IPersistStorage::Load</a> method or the <a href="/windows/desktop/api/objidl/nf-objidl-ipersiststorage-initnew">IPersistStorage::InitNew</a> method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The object was not loaded due to lack of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The object was not loaded due to some reason other than a lack of memory.

</td>
</tr>
</table>

## -remarks

This method initializes an object from an existing storage. The object is placed in the loaded state if this method is called by the container application. If called by the default handler, this method places the object in the running state.

Either the default handler or the object itself can hold onto the <a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> pointer while the object is loaded or running.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Rather than calling <b>IPersistStorage::Load</b> directly, you typically call the <a href="/windows/desktop/api/ole2/nf-ole2-oleload">OleLoad</a> helper function which does the following:

<ol>
<li>Create an uninitialized instance of the object class.</li>
<li>Query the new instance for the <a href="/windows/desktop/api/objidl/nn-objidl-ipersiststorage">IPersistStorage</a> interface.</li>
<li>Call <b>Load</b> to initialize the object from the existing storage.</li>
</ol>
You also call this method indirectly when you call the <a href="/windows/desktop/api/ole2/nf-ole2-olecreatefromdata">OleCreateFromData</a> function or the <a href="/windows/desktop/api/ole/nf-ole-olecreatefromfile">OleCreateFromFile</a> function to insert an object into a compound file (as in a drag-and-drop or clipboard paste operation).

The container should cache the <a href="/windows/desktop/api/objidl/nn-objidl-ipersiststorage">IPersistStorage</a> pointer for use in later operations on the object.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Your implementation should perform the following steps to load an object:

<ol>
<li>Open the object's streams in the storage object, and read the necessary data into the object's internal data structures.</li>
<li>Clear the object's dirty flag.</li>
<li>Call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> method and cache the passed in storage pointer.</li>
<li>Keep open and cache the pointers to any streams or storages that the object will need to save itself to this storage.</li>
<li>Perform any other default initialization required for the object.</li>
</ol>
Steps 3 and 4 are particularly important for ensuring that the object can save itself in low memory situations. Holding onto pointers to the storage and stream interfaces guarantees that a save operation to this storage will not fail due to insufficient memory.

Your implementation of this method should return the CO_E_ALREADYINITIALIZED error code if it receives a call to either the <a href="/windows/desktop/api/objidl/nf-objidl-ipersiststorage-initnew">IPersistStorage::InitNew</a> method or the <b>IPersistStorage::Load</b> method after it is already initialized.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-ipersiststorage">IPersistStorage</a>



<a href="/windows/desktop/api/ole2/nf-ole2-oleload">OleLoad</a>