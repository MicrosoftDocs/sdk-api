---
UID: NF:objidl.IPersistFile.Save
title: IPersistFile::Save
author: windows-sdk-content
description: Saves a copy of the object to the specified file.
old-location: com\ipersistfile_save.htm
tech.root: com
ms.assetid: da9581e8-98c7-4592-8ee1-a1bc8232635b
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IPersistFile interface [COM],Save method, IPersistFile.Save, IPersistFile::Save, Save, Save method [COM], Save method [COM],IPersistFile interface, _com_ipersistfile_save, com.ipersistfile_save, objidl/IPersistFile::Save
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
 - IPersistFile.Save
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPersistFile::Save


## -description


Saves a copy of the object to the specified file.


## -parameters




### -param pszFileName [in]

The absolute path of the file to which the object should be saved. If <i>pszFileName</i> is <b>NULL</b>, the object should save its data to the current file, if there is one.


### -param fRemember [in]

Indicates whether the <i>pszFileName</i> parameter is to be used as the current working file. If <b>TRUE</b>, <i>pszFileName</i> becomes the current file and the object should clear its dirty flag after the save. If <b>FALSE</b>, this save operation is a <b>Save A Copy As ...</b> operation. In this case, the current file is unchanged and the object should not clear its dirty flag. If <i>pszFileName</i> is <b>NULL</b>, the implementation should ignore the <i>fRemember</i> flag.


## -returns



If the object was successfully saved, the return value is S_OK. Otherwise, it is S_FALSE. This method can also return various storage errors.




## -remarks




This method can be called to save an object to the specified file in one of three ways:



The implementer must detect which type of save operation the caller is requesting. If the <i>pszFileName</i> parameter is <b>NULL</b>, a <b>Save</b> is being requested. If the <i>pszFileName</i> parameter is not <b>NULL</b>, use the value of the <i>fRemember</i> parameter to distinguish between a <b>Save As</b> and a <b>Save a Copy As</b>.

In <b>Save</b> or <b>Save As</b> operations, <b>IPersistFile::Save</b> clears the internal dirty flag after the save and sends <a href="https://msdn.microsoft.com/26da5e16-5790-49c0-ba63-5feee49cd4c6">IAdviseSink::OnSave</a> notifications to any advisory connections (see also <a href="https://msdn.microsoft.com/b64ceaf7-45ba-4a66-a5cf-aec352472d3d">IOleAdviseHolder::SendOnSave</a>). Also, in these operations, the object is in NoScribble mode until it receives an <a href="https://msdn.microsoft.com/eda29981-0c24-409a-8fb9-2dc2eb96d108">IPersistFile::SaveCompleted</a> call. In NoScribble mode, the object must not write to the file.

In the <b>Save As</b> scenario, the implementation should also send <a href="https://msdn.microsoft.com/ec9926fb-d69e-430c-b67d-24c52d806bb5">IAdviseSink::OnRename</a> notifications to any advisory connections (see also <a href="https://msdn.microsoft.com/64e44cab-b618-49af-bf0e-966b9eaa198a">IOleAdviseHolder::SendOnRename</a>).

In the <b>Save a Copy As</b> scenario, the implementation does not clear the internal dirty flag after the save.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
OLE does not call <b>IPersistFile::Save</b>. Typically, applications would not call it unless they are saving an object to a file directly, which is generally left to the end-user.




## -see-also




<a href="https://msdn.microsoft.com/7d34507f-8a16-43b4-8225-010798abc546">IPersistFile</a>
 

 

