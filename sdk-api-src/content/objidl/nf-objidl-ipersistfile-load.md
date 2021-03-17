---
UID: NF:objidl.IPersistFile.Load
title: IPersistFile::Load (objidl.h)
description: Opens the specified file and initializes an object from the file contents.
helpviewer_keywords: ["IPersistFile interface [COM]","Load method","IPersistFile.Load","IPersistFile::Load","Load","Load method [COM]","Load method [COM]","IPersistFile interface","_com_ipersistfile_load","com.ipersistfile_load","objidl/IPersistFile::Load"]
old-location: com\ipersistfile_load.htm
tech.root: com
ms.assetid: 8391aa5c-fe6e-4b03-9eef-7958f75910a5
ms.date: 12/05/2018
ms.keywords: IPersistFile interface [COM],Load method, IPersistFile.Load, IPersistFile::Load, Load, Load method [COM], Load method [COM],IPersistFile interface, _com_ipersistfile_load, com.ipersistfile_load, objidl/IPersistFile::Load
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
 - IPersistFile::Load
 - objidl/IPersistFile::Load
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
 - IPersistFile.Load
---

# IPersistFile::Load


## -description

Opens the specified file and initializes an object from the file contents.

## -parameters

### -param pszFileName [in]

The absolute path of the file to be opened.

### -param dwMode [in]

The access mode to be used when opening the file. Possible values are taken from the <a href="/windows/desktop/Stg/stgm-constants">STGM</a> enumeration. The method can treat this value as a suggestion, adding more restrictive permissions if necessary. If <i>dwMode</i> is 0, the implementation should open the file using whatever default permissions are used when a user opens the file.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The object could not be loaded due to a lack of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The object could not be loaded for some reason other than a lack of memory.

</td>
</tr>
</table>

## -remarks

<b>IPersistFile::Load</b> loads the object from the specified file. This method is for initialization only and does not show the object to the end user. It is not equivalent to what occurs when a user selects the <b>File Open</b> command.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
The <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-bindtoobject">BindToObject</a> method in file monikers calls this method to load an object during a moniker binding operation (when a linked object is run). Typically, applications do not call this method directly.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Because the information needed to open a file varies greatly from one application to another, the object on which this method is implemented must also open the file specified by the <i>pszFileName</i> parameter. This differs from the <a href="/windows/desktop/api/objidl/nf-objidl-ipersiststorage-load">IPersistStorage::Load</a> and <a href="/windows/desktop/api/objidl/nf-objidl-ipersiststream-load">IPersistStream::Load</a>, in which the caller opens the storage or stream and then passes an open storage or stream pointer to the loaded object.

For an application that normally uses OLE compound files, your <b>IPersistFile::Load</b> implementation can simply call the <a href="/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage">StgOpenStorage</a> function to open the storage object in the specified file. Then, you can proceed with normal initialization. Applications that do not use storage objects can perform normal file-opening procedures.

When the object has been loaded, your implementation should register the object in the running object table (see <a href="/windows/desktop/api/objidl/nf-objidl-irunningobjecttable-register">IRunningObjectTable::Register</a>).

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-ipersistfile">IPersistFile</a>