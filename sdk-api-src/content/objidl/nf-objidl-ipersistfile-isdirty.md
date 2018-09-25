---
UID: NF:objidl.IPersistFile.IsDirty
title: IPersistFile::IsDirty
author: windows-sdk-content
description: Determines whether an object has changed since it was last saved to its current file.
old-location: com\ipersistfile_isdirty.htm
tech.root: com
ms.assetid: 4f3df841-d7fe-472e-a13c-124fdf425a35
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: IPersistFile interface [COM],IsDirty method, IPersistFile.IsDirty, IPersistFile::IsDirty, IsDirty, IsDirty method [COM], IsDirty method [COM],IPersistFile interface, _com_ipersistfile_isdirty, com.ipersistfile_isdirty, objidl/IPersistFile::IsDirty
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
 - IPersistFile.IsDirty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPersistFile::IsDirty


## -description


Determines whether an object has changed since it was last saved to its current file.


## -parameters






## -returns



This method returns S_OK to indicate that the object has changed. Otherwise, it returns S_FALSE.




## -remarks



Use this method to determine whether an object should be saved before closing it. The dirty flag for an object is conditionally cleared in the <a href="https://msdn.microsoft.com/da9581e8-98c7-4592-8ee1-a1bc8232635b">IPersistFile::Save</a> method.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
OLE does not call <b>IsDirty</b>. Applications would not call it unless they are also saving an object to a file.

You should treat any error return codes as an indication that the object has changed. Unless this method explicitly returns S_FALSE, assume that the object must be saved.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
An object with no contained objects simply checks its dirty flag to return the appropriate result.

A container with one or more contained objects must maintain an internal dirty flag that is set when any of its contained objects has changed since it was last saved. To do this, the container should maintain an advise sink by implementing the <a href="https://msdn.microsoft.com/bc9f217a-75bd-4155-9d00-df44b00cf0e5">IAdviseSink</a> interface. Then, the container can register each link or embedding for data change notifications with a call to <a href="https://msdn.microsoft.com/be9891d4-aad3-42a0-8c8e-4b86091ff03b">IDataObject::DAdvise</a>. Then, the container can set its internal dirty flag when it receives an <a href="https://msdn.microsoft.com/834a5328-3a1f-4edb-aad0-be8ab87acb04">IAdviseSink::OnDataChange</a> notification. If the container does not register for data change notifications, the <b>IPersistFile::IsDirty</b> implementation would call <a href="https://msdn.microsoft.com/604e044f-cede-486e-8b17-c62a1cfd1d28">IPersistStorage::IsDirty</a> for each of its contained objects to determine whether they have changed.

The container can clear its dirty flag whenever it is saved, as long as the file to which the object is saved is the current working file after the save. Therefore, the dirty flag would be cleared after a successful <b>Save</b> or <b>Save As</b> operation, but not after a <b>Save A Copy As . . .</b> operation.




## -see-also




<a href="https://msdn.microsoft.com/834a5328-3a1f-4edb-aad0-be8ab87acb04">IAdviseSink::OnDataChange</a>



<a href="https://msdn.microsoft.com/be9891d4-aad3-42a0-8c8e-4b86091ff03b">IDataObject::DAdvise</a>



<a href="https://msdn.microsoft.com/7d34507f-8a16-43b4-8225-010798abc546">IPersistFile</a>
 

 

