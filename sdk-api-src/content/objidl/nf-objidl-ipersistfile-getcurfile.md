---
UID: NF:objidl.IPersistFile.GetCurFile
title: IPersistFile::GetCurFile (objidl.h)
description: Retrieves the current name of the file associated with the object. If there is no current working file, this method retrieves the default save prompt for the object.
helpviewer_keywords: ["GetCurFile","GetCurFile method [COM]","GetCurFile method [COM]","IPersistFile interface","IPersistFile interface [COM]","GetCurFile method","IPersistFile.GetCurFile","IPersistFile::GetCurFile","_com_ipersistfile_getcurfile","com.ipersistfile_getcurfile","objidl/IPersistFile::GetCurFile"]
old-location: com\ipersistfile_getcurfile.htm
tech.root: com
ms.assetid: 61f1751d-47ce-4b3f-9876-24ddd542dacb
ms.date: 12/05/2018
ms.keywords: GetCurFile, GetCurFile method [COM], GetCurFile method [COM],IPersistFile interface, IPersistFile interface [COM],GetCurFile method, IPersistFile.GetCurFile, IPersistFile::GetCurFile, _com_ipersistfile_getcurfile, com.ipersistfile_getcurfile, objidl/IPersistFile::GetCurFile
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
 - IPersistFile::GetCurFile
 - objidl/IPersistFile::GetCurFile
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
 - IPersistFile.GetCurFile
---

# IPersistFile::GetCurFile


## -description

Retrieves the current name of the file associated with the object. If there is no current working file, this method retrieves the default save prompt for the object.

## -parameters

### -param ppszFileName [out]

The path for the current file or the default file name prompt (such as *.txt). If an error occurs, <i>ppszFileName</i> is set to <b>NULL</b>.

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
A valid absolute path was returned successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The default save prompt was returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The operation failed due to insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The operation failed due to some reason other than insufficient memory.

</td>
</tr>
</table>

## -remarks

This method allocates memory for the string returned in the <i>ppszFileName</i> parameter using the <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-alloc">IMalloc::Alloc</a> method. The caller is responsible for calling the <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-free">IMalloc::Free</a> method to free the string. Both the caller and this method use the OLE task allocator provided by a call to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetmalloc">CoGetMalloc</a>.

The file name returned in <i>ppszFileName</i> is the name specified in a call to <a href="/windows/desktop/api/objidl/nf-objidl-ipersistfile-load">IPersistFile::Load</a> when the document was loaded; or in <a href="/windows/desktop/api/objidl/nf-objidl-ipersistfile-savecompleted">IPersistFile::SaveCompleted</a> if the document was saved to a different file.

If the object does not have a current working file, it should provide the default prompt that it would display in a <b>Save As</b> dialog box. For example, the default save prompt for a word processor object could be

"*.txt".

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
OLE does not call the <b>GetCurFile</b> method. Applications would not call this method unless they are also calling the save methods of this interface.

In saving the object, you can call this method before calling <a href="/windows/desktop/api/objidl/nf-objidl-ipersistfile-save">IPersistFile::Save</a> to determine whether the object has an associated file. If this method returns S_OK, you can then call <b>IPersistFile::Save</b> with a <b>NULL</b> filename and a <b>TRUE</b> value for the <i>fRemember</i> parameter to tell the object to save itself to its current file. If this method returns S_FALSE, you can use the save prompt returned in the <i>ppszFileName</i> parameter to ask the end user to provide a file name. Then, you can call <b>IPersistFile::Save</b> with the file name that the user entered to perform a <b>Save As</b> operation.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-ipersistfile">IPersistFile</a>