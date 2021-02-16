---
UID: NF:objidl.IPersistStorage.Save
title: IPersistStorage::Save (objidl.h)
description: Saves an object, and any nested objects that it contains, into the specified storage object. The object enters NoScribble mode.
helpviewer_keywords: ["IPersistStorage interface [COM]","Save method","IPersistStorage.Save","IPersistStorage::Save","Save","Save method [COM]","Save method [COM]","IPersistStorage interface","_com_ipersiststorage_save","com.ipersiststorage_save","objidl/IPersistStorage::Save"]
old-location: com\ipersiststorage_save.htm
tech.root: com
ms.assetid: 3a200812-48d9-4202-987a-1400aa66191c
ms.date: 12/05/2018
ms.keywords: IPersistStorage interface [COM],Save method, IPersistStorage.Save, IPersistStorage::Save, Save, Save method [COM], Save method [COM],IPersistStorage interface, _com_ipersiststorage_save, com.ipersiststorage_save, objidl/IPersistStorage::Save
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
 - IPersistStorage::Save
 - objidl/IPersistStorage::Save
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
 - IPersistStorage.Save
---

# IPersistStorage::Save


## -description

Saves an object, and any nested objects that it contains, into the specified storage object. The object enters NoScribble mode.

## -parameters

### -param pStgSave [in]

An <a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> pointer to the storage into which the object is to be saved.

### -param fSameAsLoad [in]

Indicates whether the specified storage is the current one, which was passed to the object by one of the following calls: <a href="/windows/desktop/api/objidl/nf-objidl-ipersiststorage-initnew">IPersistStorage::InitNew</a>, <a href="/windows/desktop/api/objidl/nf-objidl-ipersiststorage-load">IPersistStorage::Load</a>, or <a href="/windows/desktop/api/objidl/nf-objidl-ipersiststorage-savecompleted">IPersistStorage::SaveCompleted</a>.

This parameter is set to <b>FALSE</b> when performing a <b>Save As</b> or <b>Save A Copy To</b> operation or when performing a full save. In the latter case, this method saves to a temporary file, deletes the original file, and renames the temporary file.

This parameter is set to <b>TRUE</b> to perform a full save in a low-memory situation or to perform a fast incremental save in which only the dirty components are saved.

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
<dt><b>STG_E_MEDIUMFULL</b></dt>
</dl>
</td>
<td width="60%">
The object was not saved because of a lack of space on the disk.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The object could not be saved due to errors other than a lack of disk space.

</td>
</tr>
</table>

## -remarks

This method saves an object, and any nested objects it contains, into the specified storage. It also places the object into NoScribble mode. Thus, the object cannot write to its storage until a subsequent call to the <a href="/windows/desktop/api/objidl/nf-objidl-ipersiststorage-savecompleted">IPersistStorage::SaveCompleted</a> method returns the object to Normal mode.

If the storage object is the same as the one it was loaded or created from, the save operation may be able to write incremental changes to the storage object. Otherwise, a full save must be done.

This method recursively calls the <b>IPersistStorage::Save</b> method, the <a href="/windows/desktop/api/ole2/nf-ole2-olesave">OleSave</a> function, or the <a href="/windows/desktop/api/objidl/nf-objidl-istorage-copyto">IStorage::CopyTo</a> method to save its nested objects.

This method does not call the <a href="/windows/desktop/api/objidl/nf-objidl-istorage-commit">IStorage::Commit</a> method. Nor does it write the CLSID to the storage object. Both of these tasks are the responsibilities of the caller.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Rather than calling <b>IPersistStorage::Save</b> directly, you typically call the <a href="/windows/desktop/api/ole2/nf-ole2-olesave">OleSave</a> helper function which performs the following steps:

<ol>
<li>Call the <a href="/windows/desktop/api/coml2api/nf-coml2api-writeclassstg">WriteClassStg</a> function to write the class identifier for the object to the storage.</li>
<li>Call the <b>IPersistStorage::Save</b> method.</li>
<li>If needed, call the <a href="/windows/desktop/api/objidl/nf-objidl-istorage-commit">IStorage::Commit</a> method on the storage object.</li>
</ol>
Then, a container application performs any other operations necessary to complete the save and calls the <a href="/windows/desktop/api/objidl/nf-objidl-ipersiststorage-savecompleted">SaveCompleted</a> method for each object.

If an embedded object passes the <b>IPersistStorage::Save</b> method to its nested objects, it must receive a call to its <a href="/windows/desktop/api/objidl/nf-objidl-ipersiststorage-savecompleted">IPersistStorage::SaveCompleted</a> method before calling this method for its nested objects.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-ipersiststorage">IPersistStorage</a>



<a href="/windows/desktop/api/ole2/nf-ole2-olesave">OleSave</a>