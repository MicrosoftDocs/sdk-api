---
UID: NF:objidl.IPersistFile.Load
title: IPersistFile::Load method
author: windows-driver-content
description: Opens the specified file and initializes an object from the file contents.
old-location: com\ipersistfile_load.htm
old-project: com
ms.assetid: 8391aa5c-fe6e-4b03-9eef-7958f75910a5
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IPersistFile, IPersistFile interface [COM], Load method, IPersistFile::Load, Load method [COM], Load method [COM], IPersistFile interface, Load,IPersistFile.Load, _com_ipersistfile_load, com.ipersistfile_load, objidl/IPersistFile::Load
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
req.typenames: THDTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ObjIdl.h
api_name:
-	IPersistFile.Load
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPersistFile::Load method


## -description


Opens the specified file and initializes an object from the file contents.


## -parameters




### -param pszFileName [in]

The absolute path of the file to be opened.


### -param dwMode [in]

The access mode to be used when opening the file. Possible values are taken from the <a href="https://msdn.microsoft.com/15a35da9-332a-46e1-9190-500c95e26f59">STGM</a> enumeration. The method can treat this value as a suggestion, adding more restrictive permissions if necessary. If <i>dwMode</i> is 0, the implementation should open the file using whatever default permissions are used when a user opens the file.


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
The <a href="https://msdn.microsoft.com/b5ce39ff-3387-4f72-9aea-5a26eed3810c">BindToObject</a> method in file monikers calls this method to load an object during a moniker binding operation (when a linked object is run). Typically, applications do not call this method directly.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Because the information needed to open a file varies greatly from one application to another, the object on which this method is implemented must also open the file specified by the <i>pszFileName</i> parameter. This differs from the <a href="https://msdn.microsoft.com/34379b8d-4e00-49cd-9fd1-65f88746c61a">IPersistStorage::Load</a> and <a href="https://msdn.microsoft.com/351e1187-9959-4542-8778-925457c3b8e3">IPersistStream::Load</a>, in which the caller opens the storage or stream and then passes an open storage or stream pointer to the loaded object.

For an application that normally uses OLE compound files, your <b>IPersistFile::Load</b> implementation can simply call the <a href="https://msdn.microsoft.com/5ff18dc8-b24f-42bb-8c32-efc4d3696687">StgOpenStorage</a> function to open the storage object in the specified file. Then, you can proceed with normal initialization. Applications that do not use storage objects can perform normal file-opening procedures.

When the object has been loaded, your implementation should register the object in the running object table (see <a href="https://msdn.microsoft.com/40f815b2-dfea-416c-aae1-7ba3a710ad91">IRunningObjectTable::Register</a>).




## -see-also




<a href="https://msdn.microsoft.com/7d34507f-8a16-43b4-8225-010798abc546">IPersistFile</a>
 

 

