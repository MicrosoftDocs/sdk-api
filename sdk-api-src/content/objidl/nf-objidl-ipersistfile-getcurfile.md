---
UID: NF:objidl.IPersistFile.GetCurFile
title: IPersistFile::GetCurFile
author: windows-sdk-content
description: Retrieves the current name of the file associated with the object. If there is no current working file, this method retrieves the default save prompt for the object.
old-location: com\ipersistfile_getcurfile.htm
tech.root: com
ms.assetid: 61f1751d-47ce-4b3f-9876-24ddd542dacb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetCurFile, GetCurFile method [COM], GetCurFile method [COM],IPersistFile interface, IPersistFile interface [COM],GetCurFile method, IPersistFile.GetCurFile, IPersistFile::GetCurFile, _com_ipersistfile_getcurfile, com.ipersistfile_getcurfile, objidl/IPersistFile::GetCurFile
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IPersistFile.GetCurFile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



This method allocates memory for the string returned in the <i>ppszFileName</i> parameter using the <a href="https://msdn.microsoft.com/c9c9bdac-965f-4b18-9338-28a025930480">IMalloc::Alloc</a> method. The caller is responsible for calling the <a href="https://msdn.microsoft.com/d65411ea-13d5-4932-a757-d897311e9e28">IMalloc::Free</a> method to free the string. Both the caller and this method use the OLE task allocator provided by a call to <a href="https://msdn.microsoft.com/d1d09fbe-ca5c-4480-b807-3afcc043ccb9">CoGetMalloc</a>.

The file name returned in <i>ppszFileName</i> is the name specified in a call to <a href="https://msdn.microsoft.com/8391aa5c-fe6e-4b03-9eef-7958f75910a5">IPersistFile::Load</a> when the document was loaded; or in <a href="https://msdn.microsoft.com/eda29981-0c24-409a-8fb9-2dc2eb96d108">IPersistFile::SaveCompleted</a> if the document was saved to a different file.

If the object does not have a current working file, it should provide the default prompt that it would display in a <b>Save As</b> dialog box. For example, the default save prompt for a word processor object could be

"*.txt".

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
OLE does not call the <b>GetCurFile</b> method. Applications would not call this method unless they are also calling the save methods of this interface.

In saving the object, you can call this method before calling <a href="https://msdn.microsoft.com/da9581e8-98c7-4592-8ee1-a1bc8232635b">IPersistFile::Save</a> to determine whether the object has an associated file. If this method returns S_OK, you can then call <b>IPersistFile::Save</b> with a <b>NULL</b> filename and a <b>TRUE</b> value for the <i>fRemember</i> parameter to tell the object to save itself to its current file. If this method returns S_FALSE, you can use the save prompt returned in the <i>ppszFileName</i> parameter to ask the end user to provide a file name. Then, you can call <b>IPersistFile::Save</b> with the file name that the user entered to perform a <b>Save As</b> operation.




## -see-also




<a href="https://msdn.microsoft.com/7d34507f-8a16-43b4-8225-010798abc546">IPersistFile</a>
 

 

